---
layout: single
title: "Multi-Modal LLM Capabilities"
excerpt: "LLMs can now analyze images and generate detailed narratives with minimal input. I tested this by having Claude Sonnet 3.5 interpret everyday scenes and historical documents — producing rich, context-aware stories. The potential for real-world applications is enormous."
category: "Building with LLMs"
tags: ["multimodal", "image-analysis", "claude-sonnet", "narratives", "visual-ai"]
---

Multi-modal LLMs -- and specifically the incorporation of vision models -- is such an amazing unlock for what is possible. With limited prompting and no custom infrastructure, you can do amazing stuff already. Simply uploading an image to an LLM and asking 'what's happening here?' gives interesting results. 

Here are two fun examples I tried this morning with Claude Sonnet 3.5. I'm eager for more people to **understand what's possible** with these technologies. These two examples are certainly toy examples, and there's no 'product' being built around it. But I am hopeful that the more people who understand what's possible -- combined with domain expertise and knowledge of what problems should be solved with these technologies -- will lead to some pretty incredible products and use-cases.

### Example 1

>Please make up a story about what you see in the image. What has likely occurred here before we see what we are seeing
>
> <img src="/docs/assets/images/mutli-modal-llms/1.jpeg" width="300px" height="500px"/>

**Result**
>Based on the scene in the image, here's a possible story of what might have occurred: It seems a hectic morning routine has just taken place in this household. A parent, likely rushing to get their young child ready for school or daycare, has left evidence of their hurried preparations on the dining table. The child, let's call her Emma, was probably resistant to getting ready, more interested in playing on her tablet (the pink-cased device on the table) than eating breakfast or brushing her hair. The parent, trying to multitask, placed a small yellow bowl of cereal or snacks in front of Emma to coax her into eating while attempting to brush the child's tangled hair, hence the hair brush on the table. Meanwhile, the parent was likely trying to get ready themselves, explaining the water bottle on the table - perhaps filled hastily before heading out the door. The napkin suggests a quick wipe-up of a small spill during the morning chaos. As they finally managed to usher Emma out, the parent forgot to clear the table, leaving behind this snapshot of their morning rush. The peaceful, nicely decorated room beyond the table stands in amusing contrast to the signs of frenzied activity left behind, hinting at the daily juggle of family life and work responsibilities. Now, the house sits quiet, with only these scattered items telling the tale of the morning's lively start to the day.


### Example 2

>I want you to function as a historian and build a narrative about the person who received the degree in the attached image. Please use any resources you have to understand the time period, and other relevant details that could be helpful in creating the narrative. Please be fairly detailed in the narrative, adding details leading up to attending the university, details about attending the university, and what happened to this person after they attended. I want the story to be historically accurate. Please use your imagination and do a great job.
>
><img src="/docs/assets/images/mutli-modal-llms/2.jpeg" width="600px" height="600px"/>

**Result**
>John Joseph Sweeney received his Bachelor of Electrical Engineering degree from Cornell University on June 23, 1946. This timing is significant, as it was just after the end of World War II.
Born in the late 1920s, John likely grew up during the Great Depression. His family, like many others, may have faced economic hardships during this time. Despite these challenges, John excelled in his studies, particularly in mathematics and science.
>As a young man, John would have witnessed the technological advancements spurred by World War II. This exposure, combined with his aptitude for math and science, likely influenced his decision to pursue electrical engineering.
John entered Cornell University in the early 1940s, but his studies were likely interrupted by the war. Many young men of his generation either enlisted or were drafted into military service. If John served, he may have used the G.I. Bill to complete his education after the war.
>At Cornell, John would have studied cutting-edge electrical engineering concepts. The post-war era saw rapid advancements in electronics, and John's education would have prepared him for this evolving field.
>After graduating in 1946, John entered a booming job market. The post-war economic expansion created numerous opportunities for engineers. He might have found work in the growing telecommunications industry, helped develop early computer systems, or contributed to the expanding electrical infrastructure across the United States.
>Throughout his career, John likely witnessed and contributed to many technological advancements, from the rise of television to the early stages of the computer age. His Cornell education would have provided a strong foundation for a long and potentially innovative career in electrical engineering.

### Final Thoughts

Imagine what is possible with truly valuable use-cases, and some diligence around the prompting. What have you tried to use LLMs for? What aspects are you curious about? I'd love to hear from you, drop me a note!