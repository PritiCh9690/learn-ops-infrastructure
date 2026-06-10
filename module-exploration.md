# learn-ops-api: Service Exploration

## 1. Top-level folders in `learn-ops-api`

| Folder    | Why does this folder need to exist?                                   |
| --------- | --------------------------------------------------------------------- |
| config    | for secrets and security(Isolate sensitive API keys and passwords)    |
| templates | for Nav bar,div packages                                              |
| logs      | learning patform security and keep important passwards key for future |

## 2. Folders inside `LearningAPI`

| Folder.    | What responsibility does it own and why?                                                   |
| ---------- | ------------------------------------------------------------------------------------------ |
| fixture    | authentication package for keep all data secure                                            |
| migrations | keep students data on one place.we can add,remove student info for easy to undersatnd data |
| tests      |                                                                                            |

## 3. What is the Pipfile?

Pipfile is for dev packages and keep all data for reusable

## 4. Key packages in the Pipfile

| Package             | What functionality does it provide and why?                                                                |
| ------------------- | ---------------------------------------------------------------------------------------------------------- |
| django              | dependencies, version constraints, and required Python version                                             |
| djangorestframework | Translates complex Django models into native Python data types that can easily be rendered into JSON, XML. |
| django-allauth      | authentication, registration, account management, and social logins                                        |

## 5. What does `decorators.py` do?

modify or extend the behavior of functions or classes without altering their original code

## 6. What is a serializer, and what serializers are defined here?

Translates database data into a dictionary, which DRF then renders into a standard exchange format like JSON.

## 7. Models and what they represent

| Model | Real-world thing it represents |
| ----- | ------------------------------ |
|       |                                |
|       |                                |
|       |                                |

## 8. Views vs. viewsets

| Type    | Example class | File path |
| ------- | ------------- | --------- |
| View    | login_user    |           |
| ViewSet | CohortViewSet |           |

## 9. Serializers paired with their models

| Serializer | Model | Link |
| ---------- | ----- | ---- |
|            |       |      |
|            |       |      |

## 10. What replaces the Templates and why?

The template took Python data and turned it into an HTML page for the browser.
