a collection of prompts and templates for creating prompts that assist in research related tasks. These are arranged into playbook style folders with a predictable structure and attempt to conform to emerging best practices and patterns.


> the problem is that the broad dissemination proper design that highlights and respects limitations is essentially the end state of a deflated bubble

Sharpen your pencils.



###### `instructions.md`
this is the main file, it contains the assistant or agent level instructions for the LLM to use.

Style notes:
- these instructions should be as generic and model agnostic as possible
- instructions should assume, and respect, that the user has their own user-level prompts that may also be in play
- use task formatting (see below)

I'm still working out the right formatting 
```markdown
---
Trigger: user has sufficiently explained their goals
Instruction: define success

... detailed instructions here
```


###### `instructions-{model}.md`
this file is a varient of instructions.md tuned for a specific model and model generation.

###### context/
this directory contains supporting folders, such as example outputs, templates  or other guidance. Mostly these are Markdown files, but CSVs and PDFs seem to work well too.

### workflows, assistants, and agents

###### research plan assistant
The research plan assistant is designed to gather context from the user and  help refine that context to build a research plan. It asks context seeking questions and attempts to provoke reflection on things like what phase of work the research is a part of or what decisions this research will support.

1. establish basic intent for the research project, then open a canvas.
2. present the user with context seeking prompts, including requests for key contextual artifacts like opportunity canvasses.
3. suggest the user consult existing data or research to refine their questions.
4. suggest draft activities based on examples in the context directory (this is an area that could use a bit of expansion)
5. continue iterating with the user based on context
6. suggest next steps, such as sharing the research plan or creating a dovetail project
