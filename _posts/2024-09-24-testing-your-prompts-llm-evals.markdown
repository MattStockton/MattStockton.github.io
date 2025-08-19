---
layout: single
title: "Testing Your Prompts - Writing LLM Evals"
excerpt: "If you're using LLMs in production, you need systematic evaluations. Anthropic's notebooks and tools like PromptFoo make it easy to test prompts, compare models, and iterate quickly. LLMs are powerful, but without structured testing, you won't know if they're working as expected."
category: "Building with LLMs"
tags: ["evaluation", "testing", "prompts", "production"]
---

Anthropic created a [set of python notebooks](https://x.com/alexalbert__/status/1835717512404914401) detailing how to create prompt evaluations. The [GitHub repo is here](https://github.com/anthropics/courses/tree/master/prompt_evaluations). If you’re using a language model in your application, you should test the results of your prompts in a systematic way. It’s  not much work to do this, and it’s tremendously important to do so. There are tools to help you run the evaluations, and they don’t take much time to set up or use. I’d encourage folks to read through the notebooks linked above to build appropriate context. You can read through all of them within an hour or two. As a quick overview, I wrote a few take-aways below.

The key point to make is that like any software you’re building, you need to test it. Testing is a bit different than classical unit / regression testing, but the patterns are similar. The patterns and tools to create evals are approachable and easy to understand. If you’re building with LLMs, it’s worth your time to understand and apply these concepts — it’ll save you a ton of time in the long-run!

### My Notes

- The key components within prompt evaluation are (1) the example input (e.g the prompt to the model), (2) the golden answer (e.g. what is considered a correct answer from a model), (3) what the model actually returned, and (4) the grade (e.g. given the golden answer and the model output, how would you grade the result?)
- There are a few categories of grading. The two most approachable categories are (1) code-based grading, where you make assertions in your code (e.g. exact string matches — this is analogous to unit testing in classical software development), and (2) Using another LLM to score the output (e.g. build a different prompt that ‘grades’ the result of the first prompt)
- Anthropic provides a [workbench tool](https://console.anthropic.com/workbench) that allows you to prototype evaluations. It’s a good start, but there are also custom-built tools that give you more customization and options.
- Prompt evaluation is iterative. The point of having a systematic way to score your prompts with a quick feedback loop is to give you a clear path to *improve your prompts* - It also allows you to test different models quickly and easy (e.g. want to swap out Claude 3.5 for GPT4o?, the right prompt evaluation framework makes that really easy)
- There are a bunch of tools to help you build evaluations. A decent, light-weight open-source option is [PromptFoo](https://github.com/promptfoo/promptfoo). PromptFoo requires very little customization to get started, and relies on approachable configuration patterns. You can do almost everything in a yaml file if you’d like, but there are lots of hooks to do things like write custom evaluation logic. The UI is quite nice as well. When you run an evaluation, it’s really easy to dig into specific examples (e.g. if a specific output didn’t align with the expected result, it’s easy to click around and see why)
- For code-graded evaluations, PromptFoo has a bunch of [built-in metrics](https://www.promptfoo.dev/docs/configuration/expected-outputs/deterministic/). For example, if you want the model output to classify some text, and each piece of text can have multiple labels, there is a built-in `contains-all` construct.
- In addition to the built-in metrics, it’s easy to write custom grading functionality. You can define a python function that takes in the ‘current sample’, as well as the model output, and you can return your own score. The example given in the notebook is if you wanted the LLM to use a specific word an exact number of times in its output, you could process the output text from the model, and assert that the word appeared that number of times.
- Lots of LLM use-cases require more nuanced evaluation. For example, you might want to assert that a model response has a certain tone, or that the model response is very concise. For this use-case, PromptFoo has a built-in `llm-rubric` evaluation, where you can specify a written criteria to judge the model output, and PromptFoo will use a separate LLM prompt to check this criteria. As an example, this is the PromptFoo yaml that you can use to ensure that a model response isn’t too apologetic:
    
    ```yaml
    assert:
      - type: llm-rubric
        provider: anthropic:messages:claude-3-opus-20240229
        value: Is not apologetic
    ```
    
- When using `llm-rubric` you can click into specific samples to see why a sample passed or failed the rubric. This allows you to iterate on prompts and approaches.
- PromptFoo allows you to test multiple prompts against multiple models at the same time. So this allows you to compare prompt performance, whether you’re changing the underlying model, changing the prompt, or both.
- In addition to the built-in `llm-rubric` , there are hooks within PromptFoo to construct your own evaluation prompt. So if you have very detailed instructions on how a separate LLM prompt should be used to judge the output of the prompt you’re testing, you can code this up in python, and have PromptFoo use it.

### Final Thoughts

LLMs can feel like magic and can do things that were impossible a few years ago. They are an incredible tool to augment classical software development and machine learning. LLMs are also, by design, non-deterministic. There are some great patterns and tools to systematically test your prompting, and it doesn’t take a ton of time to get started. It’s worth your time to spin through a tutorial or two, and just give one of these tools a try.