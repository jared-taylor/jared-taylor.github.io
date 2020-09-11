---
layout: essay
type: essay
title: Ask and ye shall receive
# All dates must be YYYY-MM-DD format!
date: 2020-09-10
labels:
  - Questions
  - Answers
  - StackOverflow
---

## Knowing your audience

<img class="ui medium left spaced image" src="../images/techsupport.jpg">

In my mind, there are two types of questions that a successful IT professional should be good at asking: questions in laymens' terms (for example, asking for details of an issue a client might be experiencing) and technical questions posed to an expert. To draw from personal experience, sometimes a client who knows very little about computers as a whole might not know the difference between their monitor and the computer it is connected to. I will never forget the experience I had troubleshooting with client over the phone who said they could not get their computer to turn on. After 10 fruitless minutes, I finally gave up trying to figure it out over the phone and had to resort to a video call so I could see the problem with my own eyes, and sure enough, the client was pressing the power button on the monitor and did not even realize that it was just a screen connected to a separate machine. That might be an extreme example, but it is important to know how to ask someone to test things like network connectivity without assuming they would know their way around a command prompt, what an IP address is, and how to use the ping command. Also, when working with a client, it may be prudent to assume they are lying about everything they say they have tried. Do not ask them if they tried turning it off and turning it back on, walk them through doing so. On the flip side, when you need to ask questions to someone who may have answers to issues you can't figure out, like asking a developer about a bug you discovered in their product, it helps to know as many of the terms they might use in their troubleshooting. To illustrate an example of a good question, I'm using some highlights of a request I found on [stackoverflow](https://stackoverflow.com/questions/63704288/block-invalid-http-host-headers-in-apache-in-aws-elasticbeanstalk).

The title of the request is "Block invalid HTTP_HOST headers in Apache in AWS ElasticBeanstalk". Just in the title, the asker has already made clear what is being attempted and what technology is being used. This clear title is more likely to bring in people who have some working knowledge of web-hosting, hopefully specifically with Amazon. In the first two sentences, the asker makes clear exactly what the issue is, and provides the exact error message:

```
I have several websites running Django/Apache deployed in AWS ElasticBeanstalk.

My only problem is the hundreds of emails I receive every day with this subject:

    [Django] ERROR (EXTERNAL IP): Invalid HTTP_HOST header: WHATEVER. You may need to add WHATEVER to ALLOWED_HOSTS.

```

The continued explanation of the issue explains exactly how and why the user is attempting to block the incoming requests. They also provided snippets of their configuration, along with other examples of similar, successful implementations. To end their request, they summarize exactly where/when the issue occurs when they are attempting to resolve it on their own: "My problem is: YAML files can't make editions. I can only provide new configurations with them."

Fortunately, it looks like the detailed presentation of the issue aided in finding a suitable answer from someone who was able to recognize all the specific tools the asker is using. The response, which was marked by the asker as the best answer, starts by mentioning the exact specific issue that the asker mentioned at the end of their post:

```
Since I haven't found any better approach using YAML files, I am using a Python script to modify the original Apache wsgi.conf file in the most agnostic way I can think of (no matters if Amazon modifies it in the future).

I share it here in case anyone can find it useful. With this approach, you don't have to hardcode the hosts whitelist anywhere in code.
```

If this were me receiving the answer, I would already feel confident in the given advice based on the first sentence, because it mentions several of the key components the asker mentioned in describing the issue. In fact, the whole solution, which includes short but clear instructions on how to create the Python script, with examples of the code. 

## Conclusion

Regardless of whether you are asking questions to a tech-newbie, or asking an expert for advice, you need to be able to efficiently communicate the following questions: what specifically is not working, when does it not work, what indicates it is not working (error messages or symptoms), and what has been tried already. Generally, the more you can narrow down the specifics of an issue when asking a question, the more likely you are to receive an answer that is succinct and accurate. Specifically, the aim should be to provide enough information that a person answering need not ask any additional information about the issue. If your question requires more questions in response, it means you are delaying an answer or are getting an answer that may be vague or not specific to your issue.
