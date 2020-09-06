---
title: August 30th, 2020
---

## TODO Find referrals for paypal, IBM, Netflix, linkedin (ken guan).

## [[PROJECT]] Electric info card
### A quick scan you can know the person's information.

### Automatically add people to facebook / messenger, and everything you want to.

### The one-stop adding people software, just like wechat.

### Can add group easily based on physical location.

## [[CS194]] Start [[Project 1: Colorizing the Prokudin-Gorskii Photo Collection]]
### https://inst.eecs.berkeley.edu/~cs194-26/fa20/hw/proj1/

### Python starter code:
#### ```javascript
# CS194-26 (CS294-26): Project 1 starter Python code

# these are just some suggested libraries
# instead of scikit-image you could use matplotlib and opencv to read, write, and display images

import numpy as np
import skimage as sk
import skimage.io as skio

# name of the input file
imname = 'cathedral.jpg'

# read in the image
im = skio.imread(imname)

# convert to double (might want to do this later on to save memory)    
im = sk.img_as_float(im)
    
# compute the height of each part (just 1/3 of total)
height = np.floor(im.shape[0] / 3.0).astype(np.int)

# separate color channels
b = im[:height]
g = im[height: 2*height]
r = im[2*height: 3*height]

# align the images
# functions that might be useful for aligning the images include:
# np.roll, np.sum, sk.transform.rescale (for multiscale)

### ag = align(g, b)
### ar = align(r, b)
# create a color image
im_out = np.dstack([ar, ag, b])

# save the image
fname = '/out_path/out_fname.jpg'
skio.imsave(fname, im_out)

# display the image
skio.imshow(im_out)
skio.show()```

## [[Mindfulness]] Start each activity with an intention
### The intention should not be the result of the activity, like "I want to be stronger".

### It should be something that we can control, for example, "I will remain calm".  

### I can probably incorporate this into [[Roam]], and build a template out of it.

## [[CS194]] Continue with Project One and debug.
### Time - 19:40
#### Status - Start

#### Goal - Fix the alignment bug.
##### Result - Done

##### Turns out to be some pretty stupid mistakes
###### return the wrong value

###### forget to specify axises.

#### Intention - Remain not distracted.
##### Result - it has been pretty successful. I have concentrated for about 40 minutes without being interrupted.

#### Note
##### Currently the alignment function is not working as we expect.
###### ```javascript
# Score the two picture's alignment by differences.
# The lower the score the better.
# We use Sum of Squared Differences (SSD) to determine the score.
def score(a, b):
    return np.sum((a - b) ** 2)

# Align a to b, return an aligned new a.
# Align by iterating through possible different alignments,
# and returning the one with the lowest score.
def align(a, b):
    lowest = float("inf")
    lowest_image = a
    for axis in [0, 1]:
        for d in range(-20, 20):
            displaced_image = np.roll(a, d, axis)
            temp_score = score(b, displaced_image) 
            if temp_score < lowest:
                lowest = temp_score
                lowest_image = displaced_image
    return displaced_image```

###### ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fjialin-wu-roam%2FVjq-7hOl32.png?alt=media&token=463b8596-4ed2-45bc-896e-428fdee029b2)

### Time - 20:32
#### Status - Fix the alignment function, ready to start working on multi-scaling.

#### Goal - Finish multi-scaling
##### Built an naive version.

#### Intention - Remain not distracted, test out when I will feel tired.
##### Time - 20:48
###### Feeling kinda distracted, working on my acne just now, back to work.

##### Time - 21:52
###### Definitely feeling kinda tired right now

#### Note
##### Good reference: https://github.com/kaycem/cs194-26/blob/a2c14bdf581b06ca660010692cbe2cfbf6cb797b/project1/.ipynb_checkpoints/Untitled-checkpoint.ipynb

##### Fixed code:
###### ```python
# Score the two picture's alignment by differences.
# The lower the score the better.
# We use Sum of Squared Differences (SSD) to determine the score.
def score(a, b):
    return np.sum((a - b) ** 2)

# Align a to b, return an aligned new a.
# Align by iterating through possible different alignments,
# and returning the one with the lowest score.
def align(a, b):
    lowest = float("inf")
    lowest_image = a
    for x in range(-1 * WINDOW_SIZE, WINDOW_SIZE):
        for y in range(-1 * WINDOW_SIZE, WINDOW_SIZE):
            displaced_image = np.roll(np.roll(a, x, axis=0), y, axis=1)
            temp_score = score(b, displaced_image)
            if temp_score < lowest:
                lowest = temp_score
                lowest_image = displaced_image
    return lowest_image```

### Time - 21:51
#### Status - Working on multi-scaling, finish a naive version, working on improving it.

#### Note
##### I thought I am going to return an `x, y` vector instead of the actual image vector, but it turns out to be the same.

##### Will probably revert to the code that I wrote previoiusly.

##### The code for the vector version:
###### ```python
def score(a, b):
    return np.sum((a - b) ** 2)

def translate(image, vector):
    return np.roll(np.roll(image, vector[0], axis=0), vector[1], axis=1)

# Align a to b, return an aligned new a.
# Align by iterating through possible different alignments,
# and returning the one with the lowest score.
def align(a, b):
    lowest = float("inf")
    vector = [0, 0]
    for x in range(-1 * WINDOW_SIZE, WINDOW_SIZE):
        for y in range(-1 * WINDOW_SIZE, WINDOW_SIZE):
            displaced_image = translate(a, [x, y])
            temp_score = score(b, displaced_image)
            if temp_score < lowest:
                lowest = temp_score
                vector = [x, y]
    return vector
  
# The normal single align
ag = translate(g, align(g, b))
ar = translate(r, align(r, b))

im_old = np.dstack([r, g, b])
skio.imshow(im_old)
skio.show()

im_out = np.dstack([ar, ag, b])
skio.imshow(im_out)
skio.show()```

### Time - 22:33
#### Currently our approach is to rescale to the smallest => align => rescale up => align => rescale up ...

#### Maybe it should be rescale to the smallest => get the align vector => 

#### From [[Yibin Li]] on image pyramid.
##### Basically, an image pyramid is a multi-levels image stack, where each level contains the same image but at different scales. The top-level is the image with the smallest size, while the bottom level is the image with the original size. Each level the image is rescaled by a scale factor α (α<1) than the previous level. That's why it is called an image pyramid. You may try an image pyramid with 5 to 10 levels.

##### To search the proper displacement, first, you use some metrics to find the approximate displacement d1 (with respect to the scale factor that shrinks the image) on the top-level, then divided d1 by the scale factor α, you obtain a new range of possible displacement. If you do another search on that range of possible displacements, you will find another approximate displacement d2 on the second-top level. Doing this multiple times until you reach the bottom-most level. In this way, you will have a much smaller region to search for the displacement.
