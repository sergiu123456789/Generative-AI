# Data Validation and Output Parsing with Pydantic: Text Change Tracing

## Overview

This project demonstrates the use of **Pydantic** for robust data validation and parsing of structured output. It focuses on tracing **text changes** by comparing input and output text, and identifying the **gaps** or transformations applied.

The primary goals are:
- To validate structured data inputs and outputs using Pydantic models.
- To parse the changes between an input text and its modified output.
- To fill out or explain the gaps — i.e., what was added, removed, or transformed in the output.

---

## Project Structure

### 1. **Pydantic Models**

Define Pydantic models for:
- Input data (raw text)
- Output data (processed/modified text)
- Change log (summary of changes)

```python
from pydantic import BaseModel
from typing import List, Dict, Union, Optional, Any

class scientist(BaseModel):
  name: str
  field: str
  known_for: list[str]
  birth_year: int
