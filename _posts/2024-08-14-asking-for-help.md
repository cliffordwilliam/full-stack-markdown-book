---
layout: post
title:  "Asking For Help"
---

Lesson contents:

* TOC
{:toc}

## Introduction

When asking programming questions, your questions must be well-formed and has as much context as needed to get the most out of it. Here we discuss how to ask programming questions effectively.

## Lesson overview

- Techniques for asking programming questions.
- How to avoid asking bad questions.
- Be able to ask good programming questions.

## Tips for getting the best help possible

### Always provide your code and the surrounding context

Provide as much context as possible like your code, error messages and more. Then point the specific issue like the line number or certain function. This avoid back and forth questions and frustration. The more context you add, the better answer you get.

### Ask about the problem at hand, not the solution itself

Do not ask for the answer, ask on a specific thing that you are trying to do. Share your attempt so that people know what you have tried so they will not suggest the same thing and does not have to start from 0. Or if you are really stuck, you can let people know too and they will tell you what to research on to help you start. You can also share your pseudo code to share your current thought process.

### Don't take asking for more context to heart

Jangan masuk ati kalo orang minta lebih detail.

Some things seem obvious to you but it is not, expert knows that the most trivial thing have a significant impact on others. So when people asks for more context just give it to them.

## Outside sources

Section from here on out are from outside sources.

## Do not ask to ask, Just ask

Do not ask Any Java experts around? This is asking others to take responsibility because if they are mistaken they they are not an expert right. This is also bad since you filter out others from answering. And this is also lazy, if you are not willing to put in the work in asking then others will not put in the work to answering. Also being more explicit on what you are asking can attract interest from others that in turn invites more people to answer your question.

## XY Problem

This is when you ask for your attempted solution rather than the actual issue. Doing this wastes to much time and energy for everyone. Do not ask on how to do a certain solution that you come up with as others will find it odd rather just ask on the issue at hand. Because others will spend time trying to make your odd solution work only to realize that there is a more easier common solution to the real issue.

Do not get stuck thinking that the solution you think of is the one and only. Instead share the attempted solution and focus on the main issue.

## How to Ask Technical Question

### Before asking a question

#### Do your own research

Before asking do your own research and take time to prepare the question. The more time you invest the easier for others to help you.

#### Help yourself

You can solve your own problem you just lack experience on where and what to look.

This section reference is [here](https://www.theodinproject.com/guides/community/before_asking)

Always put 100% effort and make asking as a last resort, you want to be independent.

Exercises here forces you to research yourself, this is how we do things at work.

Break the problem down into small pieces and write the pseudo code.

Then research the small pieces problems with google. Like how to get random item from list, not how to make rock paper scissor with javascript. Here is how to use google to solve programming questions, the reference is [here](https://old.codinginflow.com/google-programming-questions).

Do not limit yourself to this tip, find more on how to better use Google yourself.

Say you are learning a new concept in Android, get general idea like what is this about? What is it used for? How do people use it in code? What is the common problems people had with it? What is the recent changes? Typing **Android [topic]** and **Android [topic] tutorial**. Visit the documentations that appears near the top and see the part you need. Then read lots blog posts and tutorials about it. Medium blog posts have better quality but not all are good. Do not use 1 source only, so that you get to see different approaches from different people.

Next you narrow the time span, as things get outdated fast in programming. Google search with time span set to "last year" in the "Tools" menu under the search box. This is up to date enough. If there are few results then use 2 or 3 years. Skip this if you are looking for core concepts, basic things that does not change. Only do this to things that gets updated.

You can use quotation marks to search for specific phrases, do this after you get a better idea after diving into a topic. This will search for that exact phrase. E.g. when you search Coding in Flow, it will results with things that has either the word coding or flow in it or even related words like programming. If you want to know the proper naming convention for key constant, using *SharedPreference key constant naming convention* will not work well. This is a very specific topic where it is unlikey for someone to write a blog about it. But you know in Java we use "static final" to declare a constant so *SharedPreferences "static final String"* will get you want you want. Use Ctrl + F in a page to jump for the hit word again. Filter out the right answer in your search result, if a user from Stackoverflow gets more rating it is more likely to be right than random posts. So use quotation marks for unique words, and keywords, so if you read that a class uses prominent colors, you can use prominent colors as a key word to elaborate further on what it is.

You can exclude words with the "-", If say the thing you want to study is often implemented in Singleton but you want an example that does not use it in a Singleton then you can type *Android Volley tutorial -Singleton*. That will hit any result that does not have the work Singleton in it. You can exclude a whole website too, like if you want to see from blog posts and not Stackoverflow.

You can use image search too, let's say you want to make an alert dialog. There are many guides on this but if you want a specific tutorial on how to make one that has a button in it then you can use the image search. Visit the page that has that image. This method is also good to see the name of things that you do not know of, is it called a toast or a pop up? Take a screenshot of it and see what the result says.

This line marks the end of the googling tips section above.

Read your error messages. Copy and paste the relevant part into search engine and learn what it is. Most errors have been encountered by someone online.

Triple check terminal commands. If you encountered a problem while setting up something from a guide:

- Re-read the whole guide again.
- Check your terminal history to see if you skipped something.
- Copy and paste from guide to prevent typo.
- Use `pwd` to see if you are in the right place.

Review previous lessons to see if the answer is there.

Check for typos, use [VS Code's IntelliSene](https://code.visualstudio.com/docs/editor/intellisense)

Debug your code to see what is the issue, look at the variables at every point. Bug means there is a mistake in your instruction to your computer.

Read the documentation thoroughly, most issues are from misunderstanding on what is written in the manual.

Take a break, if you are tired do not push yourself it is not beneficial. In dissolve mode new ideas and solutions come to mind. When you are in the toilet is when ideas come in.

Talk through your code line by line, so pretend that you are explaining it to someone. Do this after taking a break and you will see things that you did not see before.

Go through each tip above and use it until it is natural. Only when you have tried all the tips above and still encountered a problem, then you can ask.

If you are asking in Discord, use the right channels, you can ask curriculum-related questions in #odin-general but it tends to get burried since it is busy.

### Prepare your question

Invest time in preparing to make other help you easier.

#### 1.Provide code, pseudo-code, or other relevant information

Provide your pseudo-code using these external services:
- [CodePen](https://codepen.io/) for basic HTML/CSS/Javascript
- [Replit](https://replit.com/) for Javascript/Ruby
- [CodeSandbox](https://codesandbox.io/) for Webpack/React
- [Pastebin](http://pastebin.com/) for error messages or server output
- Provide screenshot when you can also. But do not tell others to download something to help you, downloading things are not something others want to do as it may be malicious.

If you have question before having any code yet, then provide your pseudo code.

You can also share a link to GitHub repository, share the file names, method names and so on.

If you need to share what you see you can use a screenshot. Do not take a physical photo of your computer screen, these are low quality and is hard to read.

Also never share files that requires other people to download, no one can tell if the inside has malicious things like malware.

#### 2. Explain the problem

Explain the issue and how to replicate the issue or bug consistently. Share what it is that you want to solve. People then can see if you are on the right track or not.

#### 4. Describe what you are expecting

Tell others what you expect or want to happen and why.

#### 5. Summarize what you have tried

Show your theories of what is happening, what you had investigated, the results you had after trying different solutions, any findings during debugging, to pinpoint where the issue comes from.

### After Posting Your Question

People will answer not with the answer but rather they will point you to a path like a website to where you should try to go next in search for your own solution.

Be present after asking a question as you will need to participate in the discussion, while you wait for others to answer you can continue to troubleshoot. Edit your posted question with updates on the things that you have tried. You can repost again once it gets burried or direct people to the channel that you asked in.

Once someone answered do not ask follow up question you should start research instead. You have to put in effort and only then others will help you again. Put effort and then ask. People will not help if you do not put effort yourself.

Also by taking the time to prepare your detailed question most of the time you can solve your own issue as you are preparing. If this did happen you can add this to your readme.

Here is another [link](https://stackoverflow.com/help/how-to-ask) for asking questions properly in Stack Overflow's standard.
