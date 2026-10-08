# HW03 — MongoDB Atlas Coursework

A learning repository based on the [MongoDB University Atlas Python starter](https://github.com/mongodb-university/atlas_starter_python). It demonstrates connecting with PyMongo and performing create, read, update, and delete operations on sample recipes.

**Stack:** Python · PyMongo · MongoDB Atlas  
**Stage:** starter exercise; the connection placeholder must be configured before execution.

## What the script demonstrates

- Connect to an Atlas cluster.
- Insert a group of recipe documents.
- Read all recipes and find one by ingredient.
- Update preparation time.
- Delete selected recipes.

## Setup and use

```bash
git clone https://github.com/dylanf32/HW03.git
cd HW03
python -m venv .venv
python -m pip install pymongo dnspython
```

Activate the virtual environment before installing dependencies: `source .venv/bin/activate` on macOS/Linux or `.\.venv\Scripts\Activate.ps1` on Windows.

In [atlas-starter.py](atlas-starter.py), replace the literal `<Your Atlas Connection String>` placeholder with a valid Python string or an environment-variable lookup. The placeholder is intentionally unfinished Python syntax.

For example, use a local environment variable instead of committing credentials:

```python
import os
client = pymongo.MongoClient(os.environ["MONGODB_URI"])
```

Configure an Atlas database user and network access for your machine, set `MONGODB_URI` locally, and then run:

```bash
python atlas-starter.py
```

**Data behavior:** the example drops the `myDatabase.recipes` collection before inserting sample records and later deletes two sample recipes. Use a disposable practice database.

## Repository contents

| File | Purpose |
| --- | --- |
| [atlas-starter.py](atlas-starter.py) | Atlas connection and recipe CRUD exercise |
| `README.md` | Project overview and setup |

## Attribution

The starter code and original tutorial come from MongoDB University. This repository is maintained by [Dylan Ferrer](https://github.com/dylanf32) for learning and coursework.
