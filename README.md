# React-and-FastAPI-Template

## Getting started

Below is some guidance for getting started on the task.

## Deliverables

-   [ ] Wire-frame diagrams
-   [ ] API documentation

## Project layout

The layout of the project achieved `docker-compose`.
There are directories in the root of the repository for each service.

### Directories

The directories `docs` is the place to put any documentation about the project.

The other directories, `ghi` and `api`, are services for front-end and back-end.

Inside of `ghi` is a minimal React app that has an "under construction" page.
This app is written using the [Vite](https://vitejs.dev/) bundler. The example
code is also using [jsdoc](https://jsdoc.app/) to provide type hints for
JavaScript. There is no requirement to use JSDoc, and you will be removing
these examples and providing your own code for `App.jsx`.

Inside of `api` is a minimal FastAPI application with pre-generated directories.
`main.py` file is the entrance for FastAPI.

Also in `api` is a directory for your migrations.
If you choose to use PostgreSQL, then you'll want to use
migrations to control your database. Unlike Django, where
migrations were automatically created for you, you'll write
yours by hand using DDL. There's a sample migration
in there that creates two tables.

The Dockerfile and Dockerfile.dev run your migrations
for you automatically.

### Other files

The following project files have been created as a minimal
starting point. Please follow the guidance for each one for
a most successful project.

- `docker-compose.yaml`: there isn't much in here, just a
  simple UI service, a FastAPI service, and a db service.
  Edit this file to meet the requirements for your project
  needs.
- `.gitignore`: This is a file that prevents unwanted files
  from getting added to your repository, files like
  `pyc` files, `__pycache__`, etc. It has been set up by a
  good default configuration for Python projects.
- `.env.sample`: This file is a template to copy when
  creating environment. Create a copy called `.env` and put
  all environment variables in here without fear of it being
  committed to git (see `.env` listed in `.gitignore`).

### Installing python dependencies locally

In order for IDE's built in code completion and intelligence to
work correctly, it needs the dependencies from the requirements.txt file
installed.

To Manually Create a virtual environment and pip install the requirements.

From inside the `api` folder:

```bash
python -m venv .venv
```

Then activate the virtual environment

```bash
source .venv/bin/activate
```

And finally install the dependencies

```bash
pip install -r requirements.txt
```

Then make sure the venv is correctly selected in your IDE.

## Install Extensions (Optional)

- Prettier: <https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode>
- Black Formatter: <https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter>
