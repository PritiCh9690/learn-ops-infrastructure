# learn-ops-api: AI Prompts

## 1. Project structure

map the folder structure of this project.list all top-level directories in
this project. and list the directories inside the LearningAPI and explain
each perpose(what is each ons responsibility)

put this output in module-exploration-ai.md on Top-level folders in
learn-ops-api section

## 2. Dependencies

❯ open Pipfile. Explain why this file exists and what it does.

❯ fill in section #3 what is the Pipfile in module-exploration-ai-md
Then find django, djangorestframework, and django-allauth. For each one, explain what functionality it provides and why this project uses it.

## 3. Decorators, serializers, and models

open LearningAPI/serializers.py. What do serializers do? Why does a Django REST API need them? Explain how a serializer fits into the request/response cycle.

❯ fill this into section 6 of module-exploration-ai.md

open the models folder inside LearningAPI. What is a Django model? Pick one model and explain what real-world thing it represents and why the API needs to track that data.

 fill this into section #7 of module-exploration-ai-md

## 4. Views, viewsets, and the MTV pattern

find one example of a plain view and one example of a viewset in this project

Django uses a Model-Template-View pattern. This project has no HTML templates. What takes the template's role here, and why does that make sense for a REST API?
