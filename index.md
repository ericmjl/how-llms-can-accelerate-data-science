---
revealOptions:
  transition: slide
highlightTheme: nord
theme: black-contrast
---

# 🌟 How LLMs Can Accelerate Data Science

[Eric J. Ma](https://ericmjl.github.io/)

Moderna

---

## 🧠 LLMs are

- your most knowledgeable drafting agent <!-- .element: class="fragment" -->
- prone to mistakes <!-- .element: class="fragment" -->

*Trust but verify!* <!-- .element: class="fragment" -->

---

## ✨ LLMs Enable DS Teams to Draft Great Software

----

### 📝 Draft New Code

```python
from sklearn.ensemble import RandomForestRegressor

# Copilot will usually successfully autocomplete from here
```

----

### 📚 Draft Docstrings

```python
import pandera as pa
from .schemas import raw_data_schema

@pa.check_input(raw_data_schema)
def preprocess(df: pd.DataFrame):
    """Preprocess dataframe.

    :param df: pandas DataFrame
    """
    # Copilot is usually great at drafting out docstrings
```

----

### 🧪 Draft Tests

```python
@prompt
def draft_tests(function_body):
    """I have the following function

    {{ function_body }}

    Draft me three unit tests.
    """
```

---

## 💪 LLMs Gives Your Data Science Team Superpowers

----

### 📓 Refactor entire notebooks

```python
@prompt
def refactor(notebook_json):
    """Given the following Jupyter notebook code:

    {{ notebook_json }}

    Help me propose a suite of functions
    that can be refactored out from the notebook.
    """
```

----

### 🔍 Debug Stack Trace

```python
@prompt
def debug(stack_trace):
    """Given the following stack trace:

    {{ stack_trace }}

    Help me debug what's going on here.
    """
```

----

### 📝 Draft Long-Form Documentation

```python
@prompt
def draft_documentation(
    presentation_transcript,
    diataxis_spec,
    documentation_type
):
    """I have the following meeting transcript:

    {{ presentation_transcript }}

    Here is the Diataxis spec for {{ documentation_type }}:

    {{ diataxis_spec }}

    Please write for me the {{ documentation_type }} using
    the transcript as source material.
    """
```

----

### 🗃️ Draft Database Queries

```python
@prompt
def nl2sql(nl_request, schema):
    """Given the following database schema:

    {{ schema }}

    And the following natural language request:

    {{ nl_request }}

    Return for me the SQL necessary to satisfy the
    natural language request.
    """
```

----

### ❓ Ask Questions of Code Repos

```bash
llamabot repo chat https://github.com/webpro/reveal-md.git \
--checkout main \
--model-name gpt-4-0125-preview \
--panel
```

----

<!-- .slide: data-background-image="images/llamabot-repo-chat-panel.webp" data-background-size="contain"-->

----

### 📚 Learn a New Domain

```python
@prompt
def learn(concept, education_level):
    """You are an expert in {{ concept }}.

    I am looking to understand {{ concept }}.

    Explain it to me the way Richard Feynman would explain it
    to a student in {{ education_level }}.
    """
```

----

<!-- .slide: data-background-image="images/learn-new-topics.webp" data-background-size="contain" -->

----

### 😃 Add Emojis to Your Talk

```python
@prompt
def add_emojis(talk_md):
    """Given the following Markdown slide deck:

    {{ talk_md }}

    Add emojis to all of the title headers
    while preserving the original text.
    """
```

---

## 🚀 A Productive New World

- LLMs are an insanely great productivity tool. <!-- .element: class="fragment" -->
- Supercharge your learning and automate the boring stuff. <!-- .element: class="fragment" -->

----

## 🧩 The Hardest Routine Parts of Data Science

1. Taking the time to document our work. <!-- .element: class="fragment" -->
2. Checking correctness of our work. <!-- .element: class="fragment" -->
3. Rapidly ramping up into a new knowledge domain. <!-- .element: class="fragment" -->

*LLMs can accelerate all of the above.* <!-- .element: class="fragment" -->

---

## ⭐️ Thank You

---

## 🤔 Select reading

- [Grow DS team software development skills](https://ericmjl.github.io/blog/2024/4/5/how-to-grow-software-development-skills-in-a-data-science-team/)
- [Survey of LLM tooling](https://ericmjl.github.io/blog/2024/2/1/an-incomplete-and-opinionated-survey-of-llm-tooling/)
- [Organize and motivate a DS team](https://ericmjl.github.io/blog/2024/3/23/how-to-organize-and-motivate-a-biotech-data-science-team/)
- [Keep technically sharp as a DS team lead](https://ericmjl.github.io/blog/2024/2/25/how-to-keep-sharp-with-technical-skills-as-a-data-science-team-lead/)
