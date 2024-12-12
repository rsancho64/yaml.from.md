# yaml.from.md

import +yaml +from +markdown :

```python

"""This will render the YAML with indentation.

Alternatively, you can use a library such as `markdown-full-yaml-metadata` in Python, which allows you to parse YAML metadata from Markdown files. 
* Import the `markdown` and `yaml` libraries.
* Use the `markdown.Markdown` class with the `full_yaml_metadata` extension to parse the YAML metadata.
"""

import markdown
import yaml

md = markdown.Markdown(extensions=['full_yaml_metadata'])
text = """
---
title: What is Lorem Ipsum?
categories:
  - Lorem Ipsum
  - Stupid content
...
Lorem Ipsum is simply dummy text.
"""
md.convert(text)
print(md.Meta)
