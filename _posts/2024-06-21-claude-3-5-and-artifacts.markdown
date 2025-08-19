---
layout: single
title: "Creating an Image Classifier with Claude 3.5 and Artifacts"
excerpt: "I built a working image classifier in 20 minutes using Claude 3.5 and Artifact — handling everything from Flask API setup to model integration and Docker deployment. This experiment showed just how much LLMs can accelerate development and simplify complex workflows."
category: "Software Engineering"
tags: ["claude-artifacts", "image-classifier", "flask", "docker", "rapid-development"]
---

***This post was written primarily with ChatGPT. Using ChatGPT was part of the experiment. Can I build something moderately interesting and write a post about it -- constraining myself to an hour time limit, and only use LLMs?***

I'm always on the lookout for tools that can streamline my workflow and enhance my productivity. Recently, I decided to put Claude 3.5 with Artifacts to the test, specifically to see how well it could handle creating an image classifier with minimal input. What I found was quite impressive. In this post, I'll walk you through the steps I took, highlighting the performance of Claude 3.5 and the Artifacts feature, which turned out to be remarkably user-friendly. I was able to build and deploy a simple image classifier in about 20 minutes. [Here's the code on Github](https://github.com/MattStockton/dog_classifier)

#### Getting Started

I kicked off the project with a straightforward prompt to Claude 3.5:

>I want to create a web application API using python and flask. Can you help me with that?

Claude responded with a basic Flask web application template. From there, I refined my requirements:

>Thanks for the great start! Here's what I want the API to do:
>
>   - Implement a get request that receives an encoded version of an image
>   - Decide if that image is a dog or a cat, and return True or False, with probabilities of each class
>   - Use a trained PyTorch library to do the classification on the backend
>	
>Can you modify the code to do that?

The modifications provided by Claude were spot on. The ease with which I could articulate my needs and receive functional code was quite remarkable. I intentionally made minimal changes to the code to assess its utility for developers with varying levels of expertise.

#### Running the Flask App with Docker

Next, I needed to run the Flask application locally using Docker. My experience with Docker made this step straightforward, but I wanted to see how well Claude could assist:

>How can I run this Flask app locally using Docker?

>Once I download the Dockerfile and app.py, how do I run this?

Claude's guidance was clear and concise, making it easy to create a Dockerfile, download the necessary files, and get the Flask app running locally. The seamless integration between Claude's instructions and the Artifacts feature made the process efficient and hassle-free.

#### Interacting with the API

To test the API, I requested a script to interact with it:

>Can you give me a small python script that uses the API and loads an image file from the hard drive?

Claude provided a simple yet effective script that allowed me to load an image, send it to the API, and receive the classification results. The functionality was exactly what I needed, and the implementation was straightforward.

#### Enhancing the Model and Deployment

To push the boundaries further, I sought Claude's advice on improving the model and how I can run it:

>How can I use the same Dockerfile to run a different python script

>How can I run a python script on an existing running docker container

>How should I consider making the classification model better?


Claude offered several practical suggestions and additional code snippets, demonstrating its ability to provide robust solutions. The iterative process of seeking improvements and receiving actionable code reinforced Claude's utility for experienced developers.


#### Conclusion

In about 20 minutes, I got something working!

<img src="/docs/assets/images/claude-3-5-classifier/classifier1.png" width="400px" height="400px"/>

<img src="/docs/assets/images/claude-3-5-classifier/classifier2.png" width="400px" height="400px"/>


Testing Claude 3.5 and Artifacts with an image classifier project was a compelling experience. The tools proved to be highly effective, offering precise and practical solutions with minimal input required from me. This experiment underscored how even seasoned developers can benefit from such advanced AI tools, saving time and effort while achieving sophisticated results.

In a twist of AI synergy, I used ChatGPT to help write this blog post about my experience. The collaboration between different AI tools highlights the transformative potential of these technologies in enhancing our workflows.

For developers at any level, Claude 3.5 and Artifacts offer a powerful combination that can simplify complex tasks and open up new possibilities. I encourage fellow developers to explore these tools and see how they can enhance your projects.

Here's a screenshot of using Claude 3.5 - Check it out! It's super cool

<img src="/docs/assets/images/claude-3-5-classifier/classifier3.png" width="800px" height="800px"/>
