---
layout: single
title: "Improving Retrieval Augmented Generation Systems"
---

A recent episode of the [How AI Is Built podcast](https://podcasts.apple.com/us/podcast/from-ambiguous-to-ai-ready-improving-documentation/id1739823286?i=1000677765593), hosted by [Nicolay Gerold](https://www.linkedin.com/in/nicolay-gerold/) and featuring [Max Buckley](https://www.linkedin.com/in/maxbuckley/) from Google, explored how to improve Retrieval-Augmented Generation (RAG) systems. The discussion highlighted how documentation quality can make or break a system and emphasized strategies for addressing errors, reducing ambiguities, and creating feedback loops to refine the entire pipeline — not just the retrieval aspect.

Here are five key takeaways to help you build more effective RAG systems, from improving data inputs to ensuring precision at runtime.

## 1. Adding Context to Chunks

When chunking documents for processing, much of the original context can be lost, leading to less meaningful outputs. One possible solution, as detailed in Anthropic’s [contextual retrieval post](https://www.anthropic.com/news/contextual-retrieval), is to enrich each chunk with additional context drawn from the full document. This method ensures that each chunk provides more complete information, even in isolation.

Ways to add context include:  
- Appending or prepending a summary of the full document.  
- Including relevant adjacent paragraphs or hierarchical metadata like headings.  
- Incorporating broader contextual notes about the document’s purpose.  

For example, instead of a chunk reading, “The revenue was $43 million,” it could be expanded to say, “In this company’s Q3 filing, the revenue was $43 million.” This enriched chunk is far more informative.  

New features like **prompt caching** make it easier to implement such techniques. By caching the entire document in a prompt, you can iterate over each chunk to enrich it with context before creating embeddings. This approach not only improves retrieval performance but also enhances the quality of the LLM’s responses, and it can be fairly inexpensive.

## 2. Representing Chunks with Multiple Embeddings

Using a single embedding for each chunk can lead to limitations, especially when user query phrasing or intent varies. A more robust approach is to generate multiple embeddings for each chunk, capturing its different facets. These are just a few examples of how you might represent chunks:  

- The raw text embedding to capture the literal content.  
- A summarized version embedding to capture the chunk’s essence in fewer words.  
- Hypothetical question embeddings to represent the kinds of queries the chunk might answer.  

For instance, if a user searches for “annual revenue,” the query might better match a hypothetical question embedding than the raw text. This method bridges gaps between varied query styles and the chunk’s content, ensuring more accurate retrieval.

There’s no one-size-fits-all approach here. You might find other ways to represent chunks, depending on the specific requirements of your system or domain.

## 3. Pre-Submission LLM Checks for Documentation Quality At The Source

Building a great application that uses RAG isn’t just about retrieval — it’s about thinking holistically and addressing the entire pipeline. Often, the most impactful improvements come from upstream efforts, such as ensuring the quality of the input data. By introducing **pre-submission LLM checks**, you’re effectively building **hooks upstream** that allow LLMs to analyze and refine content before it is stored in the source system.

These checks are proactive mechanisms that ensure your documentation is clear, consistent, and structured before it becomes part of your authoritative source documentation that is 'retrievable'. They go beyond correcting grammar and spelling to evaluate:  

- **Clarity and readability**: Are sentences concise and unambiguous? Are vague pronouns (e.g., "it") replaced with clear references?  
- **Consistency**: Does the text adhere to terminology and style guidelines across documents?  
- **Structure**: Is the content organized logically with all necessary sections included?  

For example, if someone writes, “The proposal was approved,” a pre-submission LLM check could suggest rewriting this to “The board approved the Q4 proposal,” clarifying both the subject and context. Similarly, these hooks could identify inconsistent naming conventions or formatting errors, ensuring that documentation is standardized and coherent.

The advantage of placing these hooks upstream is that they significantly reduce downstream issues. Clean, high-quality input data enhances every subsequent step of the RAG process, from retrieval to final response generation. This approach often yields better results than endlessly iterating on retrieval mechanisms, as it addresses root causes rather than treating symptoms. Plus, it makes your documentation clearer for people to actually read as well.

By thinking beyond retrieval and focusing on the entire system, you can invest resources where they’ll have the greatest impact, ensuring that your RAG system operates on a solid foundation.

## 4. Runtime Consistency Checks for Precise Prompts

The ultimate goal of a RAG system is to ensure that the prompt sent to the LLM contains the most precise, succinct, and relevant content necessary to answer the query. One novel approach discussed in the podcast is to add a **runtime consistency check** for retrieved chunks. This relatively inexpensive step evaluates the chunks for issues like contradictions, ambiguities, or irrelevance before they are included in the final prompt.

Here’s how it works:  

1. Retrieve multiple chunks for a query.  
2. Use an LLM to analyze the retrieved chunks for inconsistencies or contradictions.  
3. Remove problematic chunks or re-retrieve replacements if issues are found.  

For example, if a query retrieves two chunks about a company’s revenue with conflicting figures, the LLM can flag this inconsistency. Addressing such issues ensures that the final prompt contains reliable information, avoiding potential errors in the response.

This consistency check is a cost-effective way to improve prompt quality and prevent “bad content” from distorting the final output. It’s a straightforward but powerful step to ensure the final query is as accurate and reliable as possible.

## 5. Handling Linguistic Subtleties and Internal Terminology

LLMs often struggle with subtle linguistic nuances and domain-specific jargon, which can lead to inaccurate outputs. Addressing this involves creating a clear glossary of terms and rewriting ambiguous language to be explicit and concise. Even with longer context windows in modern LLMs, clear and detailed inputs remain essential — particularly when providing a dictionary of terms.

**Practical example**: If “System X” is also known as “Backend Y” in your organization, adding a simple clarification like, “System X is the backend for Y,” ensures the LLM retrieves accurate content. Similarly, replacing vague pronouns like “it” with explicit references (e.g., “System X supports real-time updates”) improves both human and machine understanding.

While longer context windows reduce some constraints, clear, unambiguous information always enhances retrieval accuracy and ensures the system provides relevant and reliable answers.

## Conclusion

Improving a RAG system involves more than just refining retrieval — it requires a holistic approach across the entire pipeline. Strategies like contextualized chunking, multiple embeddings, pre-submission and runtime checks, and handling linguistic nuances help ensure precise and reliable outputs. By focusing on these areas, you can build a system that works seamlessly for both humans and machines.

If you’re interested in learning more, [Jason Liu](https://jxnl.co/writing/category/rag/) writes excellent content on RAG systems. His material is highly approachable and a must-read for anyone considering building or improving a system in this space.