---
title: September 5th, 2020
---

## {DONE}} Add links of Design 01 to choruses.

## [[RR03]]
### Prompt:
#### For your first programming project, you are designing an electric personal transportation conversion app (given an input of the distance and type of transport, you’ll be able to see how long it will take to travel there as well as the equivalent time using other transportation modes). Create a **persona** that would be useful in the design of PROG 01, and describe a **scenario** of usage for that app. Use your persona in the scenario. Why is it important to consider personas when designing an application?

### Note
#### Chapter 4: [[Analyzing User Research in Designing the iPhone User Experience: A User-Centered Approach to Sketching and Prototyping iPhone Apps, Suzanne Ginsburg]] (2011).
##### Analyzing user research
###### ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fjialin-wu-roam%2FawlrPov6Yl.png?alt=media&token=2fe2dc4b-8323-470c-ad6a-4bb4defcd21e)

###### PDS: Product Definition Statement

##### [[Persona]]
###### Personas are profiles of archetypal users, as opposed to profiles of actual users. They represent the needs of many users.

###### Personas allow you to keep design teams on the same page with regard to target users, and they help prevent team members from being self-referential.

###### Types of personas:
####### Primary personas - the ones that needs must be addressed

####### Secondary personas - less important

####### Negative personas - not target users

##### [[Scenario]]
###### Scenarios describe how personas may use your app to achieve their goals.

###### Things that should include in a scenario
####### ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fjialin-wu-roam%2FElfqSDnU0c.png?alt=media&token=f212b4f6-f64c-4c2a-8721-bc4a735245fd)

###### [[User Story]] vs. [[Use case]] vs. [[Scenario]]
####### [[Use case]] are much more concise than scenarios and may include aspects of
the back end. often called the "system'- They help uncover flow and usability issues in the later stages of design, but they are generally too system oriented for early-stage brainstorming. 

####### [[User Story]] are commonly used in the Agile software development process. They tend to be more feature-oriented than scenarios since they must be broken down for the "backlog".

#### [[About Face 3: The Essentials of Interaction Design]] Chapter Five - [[Persona]] and Goals
##### Don't try to make a product that satisfy all the needs for everyone.
###### Design for specific types of individual with specific needs.

###### "When you broadly and arbitrarily extend a product's functionality to include many constituencies, you increase the cognitive load and navigational overhead for all users."

###### **Software today is too often designed to please too many users, resulting in low user satisfaction.**

##### Persona solves three problems
###### The elastic user
####### The meaning behind "User" constantly changes from people to people. Everyone has a definition of his own user, and thus, it become elastic.

###### Self-referential design

###### Edge cases

##### Persona are based on researches.

##### Persona must have motivations.

##### Persona should have goals.
###### Goals motivate usage patterns.

##### Three levels of Cognitive Processing
###### Visceral - most immediate level of processing, visual & sensory aspect
####### Not design beautiful things, but design for effects
######## Effects that triggers psychological or emotional response.

###### Behavioral - middle level of processing, manage daily tasks
####### The user experience of a product or artifact, therefore, should ideally harmonize elements of visceral design and reflective design with a focus on behavioral design.

###### Reflective - involves conscious consideration and reflection on past experiences & memory.
####### Build long-term product relationships.

####### Maybe this can gather some inspirations from [[Architecture]]

##### Three types of Goals corresponding to the three levels of Cognitive process.
###### Experiences Goals
####### How someone wants to feel when using a product.
######## Feel smart or in control

######## Feel Cool, feel relaxed...

###### End Goals
####### Perform certain tasks that achieve certain things.

###### Life Goals
####### The deeper drive and long term relationship with the product.

###### ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fjialin-wu-roam%2FQKSVK0f4RU.png?alt=media&token=b7cea699-a66c-445c-a675-22c8ac9f16ad)

##### 

### 

## [[VR03]]
### First video
#### Emotional relationship
##### Wear off 

#### hardware => software. interaction design

### Second video
#### design inspired by past.

#### critical eye of the past?

### Alex Wu, Pratibha Sriram

### **Framed by these two videos, what should interaction design be addressing today?  What should it be responding to and why? How do you want to participate in this movement?**

### Based on these videos, interaction design should address and respond to changing societal movements and norms and challenge previously held conceptions about the way things should work. Especially given today’s rapidly changing social climate and more awareness brought to issues including LGBTQ rights, Black Lives Matter, etc., it is important now more than ever that we change the design of our products and technology to reflect society’s expanding emphasis on inclusivity and diversity - this is crucial to maintaining user satisfaction. As discussed by the speaker in the second video, it is not only important to design more inclusive products going forward, but also to challenge previous norms about what design should be. For example, Github initially designed the name of their main branch to be “master” but, in the light of growing awareness about slave oppression, realized this terminology was offensive and is discussing renaming this concept.

### To be more active in this movement, we need to reflect on what kinds of roles that we are already participating in this society. As computer science students, we are both the end users and the engineers / designers for future products. As users, we should actively provide feedback to the designers & engineers. We should remind them that products need to be more inclusive, more accessible, and more intuitive. Actively providing feedback is one of the most important things that we can do as users. As engineers and designers for the future products, we should always keep in mind that our society is facing lots of challenges right now. We should be aware of those issues when designing and trying to address those issues with the products that we are building. Inspired by the first video, we should also try to value the emotional relationship between the products and the users. Though the emphasis of the emotional relationship of the first video is more on the hardware design, we think it is also important to make the software feel closer and more intimate to the users. By considering accessibility issues and also inclusiveness, we will remove more and more barriers between the users and the product and provide users with a sense of belonging.

## OK. I need to depart from [[Aimhub]]. Let's write a post on slack saying how to improve upon my previous work.
### Hi everyone, it has been a fantastic ride this summer. Unfortunately, my semester is starting now. This will be one of the busiest semester in my college year, so I don't think I am able to contribute to aim anymore.

I learned a lot from Gor and Gevorg. Gevorg has showed me quite a few interesting updates on the business side of aimhub, and Gor has taught me a lot of designs and programming principles. 

For my last PR (https://github.com/aimhubio/aimde/pull/70), given the time constraint, I have tried my best to build the communication server between aim & aimde. I have successfully implemented the server at both ends of the communication. However, there's still a lingering issue that I do not know how to solve: I can see the data stored into the `TrackManager`'s `_store` successfully, however, when polling, it seems like there is some issue with threadings that stops the data from being accessed. I have cleaned up my code in that PR just now and add the polling endpoint.

It has been wonderful working and learning from y'all. Wish aimhub the best of luck in the future!

## 
