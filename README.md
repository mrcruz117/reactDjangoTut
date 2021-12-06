# Django VsCode Setup

step by step instructions to set up django and your virtual
environment(venv).
## Installation

1. check to make sure the most current version of python is installed.

```bash
python --version
```
for mac:
```bash
python3 --version
```

2. install pipenv
```bash
pip install pipenv
```
for mac:
```bash
pip3 install pipenv
```
- this is a dependancy management tool for vitural environments

## Creating a project
1. create or clone your project directory then cd there.

2. In your project directory install django

```bash
pipenv install django
```
- you should see a success message along with a path to the Virtualenv location.
Example path:
```bash
/Users/tsmith/.local/share/virtualenvs/project-a12abcd
```
3. Enter virtual environment
```bash
pipenv shell
```
4. Start project
```bash
django-admin startproject "projectname" .
```
5. Configure VSCode integrated terminal
- View->Command Palette
- search "Python: Select Interpreter"
- input path to virtual environment
    - to find:
        ```bash
        pipenv --venv
        ```
- enter venv path and append /bin/python at the end
    - example:
        ```bash
        /Users/tsmith/.local/share/virtualenvs/project-a12abcd/bin/python
        ```
6. Activate venv
```bash
source /Users/tsmith/.local/share/virtualenvs/project-a12abcd/bin/activate
```
7. You should now be able to start your server
- manage.py stores any relevant venv settings.
```bash
python manage.py runserver
```
- the server automatically runs on port 8000 but you can change that to whatever port you prefer:
        ```bash
        python manage.py runserver 3030
        ```
- control-c to stop server
8. Confirm that your server is running by visiting the admin page:

    ![server](https://assets.digitalocean.com/articles/eng_python/django/django-2-testsite.png)

## Success!!!

If you want to deactivate your venv, simply enter deactivate in the terminal:
    ```
    deactivate
    ```