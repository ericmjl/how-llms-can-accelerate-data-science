---
revealOptions:
  transition: slide
highlightTheme: nord
theme: black-contrast
---

# 🌟 How LLMs can accelerate data science

Eric J. Ma

Moderna

---

## LLMs are

- your most knowledgeable drafting agent
- prone to mistakes

*Trust but verify!*

---

## LLMs enable DS Teams to draft great software

----

### Draft new code

```python
from sklearn.ensemble import RandomForestRegressor

# Copilot will usually successfully autocomplete from here
```

----

### Draft docstrings

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

### Draft tests

```python
@prompt
def draft_tests(function_body):
    """I have the following function

    {{ function_body }}

    Draft me three unit tests.
    """
```

---

## LLMs gives your data science team superpowers

----

### Debug stack trace

```python
@prompt
def debug(stack_trace):
    """Given the following stack trace:

    {{ stack_trace }}

    Help me debug what's going on here.
    """
```

----

### Draft long-form documentation

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

### Draft database queries

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

### Ask questions of code repos

```bash
llamabot repo chat https://github.com/webpro/reveal-md.git \
--checkout main \
--model-name gpt-4-0125-preview \
--panel
```

*Work in progress, feedback much welcome!*

----

<!-- .slide: data-background-image="images/llamabot-repo-chat-panel.png" data-background-size="contain"-->

----

### Learn a new domain

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

### Add emojis to your talk

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

## A whole new world

- LLMs are

---

## The hardest routine parts of data science

1. Taking the time to document our work.
2. Checking correctness of our work.
3. Rapidly ramping up into a new knowledge domain.

*LLMs can accelerate all of the above.*

---

## ⭐️ Thank you
