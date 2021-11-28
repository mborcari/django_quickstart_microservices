**Template for python running on docker**

This template was based from https://github.com/henriquebastos/django-quickstart.

**This quickstart project considers:**

- Use pyenv and virtualenv for management environment;
- Stack Django, DjangoRest, Postgre, Pike;
- Docker and Docker-compose.
- And git!


**Command to start project from this template**
```
PROJECT_NAME=yourprojectname && \
VERSION_PYTHON=3.9 && \
mkdir $PROJECT_NAME && \
cd $PROJECT_NAME && \
pyenv virtualenv $VERSION_PYTHON $PROJECT_NAME && \
pyenv activate $PROJECT_NAME && \
pip install --upgrade pip && \
pip install django
django-admin startproject --template https://github.com/mborcari/template_python_microservices/archive/main.zip --name=Procfile,.env,pytest.ini $PROJECT_NAME . && \
pip install --prefer-binary -r requirements-dev.txt && \
git init && \
git add . && \\
git commit -m 'Initial import' && \
docker-compose up
```
