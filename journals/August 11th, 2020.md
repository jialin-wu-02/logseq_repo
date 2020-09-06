---
title: August 11th, 2020
---

## Working on my [[Personal Website]], now I will use this kind of blog like format:
### ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fjialin-wu-roam%2FGaJwIQDThe.png?alt=media&token=288b0711-e9cb-4b58-ad83-8139c68d6725)

### Also will use this font called [Oxygen Mono](https://fonts.google.com/specimen/Oxygen+Mono?category=Monospace&preview.text=About&preview.text_type=custom&sidebar.open=true&selection.family=Oxygen+Mono):
#### ```javascript
<style>
@import url('https://fonts.googleapis.com/css2?family=Oxygen+Mono&display=swap');
</style>```

## Should probably use [[Gatsby]] to build my [[Personal Website]]
### Here are links to some good tutorials:

### https://medium.com/crowdbotics/how-to-build-your-own-blog-from-scratch-with-gatsbyjs-graphql-react-and-markdown-78352c367bd1

### https://www.freecodecamp.org/news/build-a-developer-blog-from-scratch-with-gatsby-and-mdx/

## For [[Aimhub]] the task of [[Track Info and Send Data via Socket]], currently experiencing two problems:
### `dictionary changed size during iteration`
#### probably has something to do with an insertion during the time of iteration.

#### Thread safe dictionary? should be.

#### OK. Solved by using Gor's `readline`

### `json.decoder.JSONDecodeError: Extra data: line 1 column 106 (char 105)`
#### This may be solved by studying the `send_line` and `read_line` method that Gor wrote.

#### It has something to do with receiving multiple json data at once.

## [[Blog]] idea: npm vs. npx.

## Try and finally fix the [[npm]] unable to install globally issue.
### https://stackoverflow.com/questions/51967335/npm-install-permission-denied-macos

### Fix it with `sudo chown -R $USER /usr/local/lib/node_modules`

## In [[RoamFM]], an idea about [[Searchability]] is very important when using [[Roam]], since we need to make sure that all the pages are searchable.
### Also [[Repeatability]] is also key, when or what should we create a page, how should we determine this?

## [[Sedge]]
### Three kinds of management:
#### Time management (tara, trello, etc...)

#### Network management (collaboration)

#### **Engineering management 音乐工程方面的管理** 比较缺少这一块的产品 (library management)
##### 调度的东西非常多

##### 包，鼓点，包填到

##### manage 合成器的 preset，manage favorite 鼓点

##### 一首歌有很多轨道

##### 管理一些特殊的file？并且可以上传到sedge

##### 合成器的preset是否是 reusable？

##### 云端 =》同步到本地的

##### 基本都是.wav file 所以很不错的

##### 可以分类

### music producer demo
#### 灵感 =》 切片 =》 remake

### Customize的空间

### 一个notepad会更好，notion like?

## {DONE}} Fill out eecs16b lab kit form
