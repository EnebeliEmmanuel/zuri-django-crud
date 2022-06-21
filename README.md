# Task: Django crud

> ## Brief

- Create a new GitHub repository with a README.md, and Python .gitignore file.

- Clone it to your machine/computer, that will create a new folder on your computer with your repository’s content.

- Create a new virtual environment in that folder named env and install django in it.

- Create a new django project. Use your Zuriboard Student ID as the name of the project.

- Create a new application using the django startapp command. The app should be called blog.

- Add the blog app to the main_projects INSTALLED_APPS.

- Replace the content of blog/models.py with the content of this [starter file](https://github.com/TobeTek/Zuri/blob/main/starter-files/Django-CRUD/models.py). We should now have a Post model in blog/models.py.

- Create migrations for your new model using the makemigrations django command. 

- Run all migrations using, migrate django command.

- To make our Post model accessible from the admin site, register the Post model in blog/admin.py 

- In blog/views.py,  create a new view/class PostListView, which inherits django’s generic ListView,  it’s config/attributes should be:

        model = Post

- Create another view, PostCreateView, which inherits django’s generic CreateView, with attributes:

        model = Post

        fields = “__all__”

        success_url  = reverse_lazy(“blog:all”)

- Create another view, PostDetailView, which inherits django’s generic DetailView, with attributes:

        model = Post

- Create another view PostUpdateView, which inherits django’s generic UpdateView, with attributes:

        model = Post

        fields = “__all__”

        success_url  = reverse_lazy(“blog:all”)

- Create another view PostDeleteView, which inherits django’s generic UpdateView, with attributes:

        model = Post

        fields = “__all__”

        success_url  = reverse_lazy(“blog:all”)

- Time to create templates.

- Create a new folder templates under the blog app.  

- Copy all the files and folders from [here](https://github.com/TobeTek/Zuri/tree/main/starter-files/Django-CRUD/templates) to blog/templates folder.

- Create a file, blog/urls.py, if it doesn’t already exist.

- Replace the content of blog/urls.py with the content of this [file](https://github.com/TobeTek/Zuri/blob/main/starter-files/Django-CRUD/urls.py) 

- Go to your project_app/urls.py and add a new url pattern with the following content:

        path("blog/", include("blog.urls", namespace="blog"))

- Stage and Commit your Django project and push your changes to your GitHub repository. 

`Note`:

- Do not add your database (db.sqlite) to version control (GitHub). 

- Ensure your final code/submission is on the default branch of your GitHub repository.

- Submit the link to your Github repository.
#


>## Solution:

- Created a new public GitHub repository.

- Cloned repository.

        git clone https://github.com/EnebeliEmmanuel/zuri-django-crud

- Created virtual environment and activated virtual enviroment

        py -m venv env
        source env/bin/activate

- Installed django

        py -m pip install django

- Extracted installed dependencies to a file named requirements.txt

        pip freeze > requirements.txt

- Created a new Django project with my zuriboard ID as the name.
    
        django-admin startproject I4G006916U67 .

- Added secret key to an enironment variable

- Made migrations

        py manage.py migrate


- Ran the django server

        py manage.py createsuperuser

- Created a new app called blog

        py manage.py startapp blog

- Added the blog app to the I4G009584AYP project's INSTALLED_APPS in settings.py

- Replaced the content of blog/models.py with the content of this [starter file](https://github.com/TobeTek/Zuri/blob/main/starter-files/Django-CRUD/models.py)

- Made migrations

        py manage.py makemigrations
        py manage.py migrate

- Registered the Post model in the blog app admin.py

- Created the post views in blog/views.py

- Created a new folder in the blog app called templates

- Copied all the required template files from [this repo](https://github.com/TobeTek/Zuri/tree/main/starter-files/Django-CRUD/templates)

- Created a new file in the blog app called urls.py and replaced it's content with the content of this [file](https://github.com/TobeTek/Zuri/blob/main/starter-files/Django-CRUD/urls.py).

- Updated I4G006916U67/urls.py to include the blog urls

- Created dummy data and tested out the CRUD functionalities.

- Git add and commit all files.

        git add .
        git commit -m "blog"

- Pushed the local repository to the remote repository.

        git push -u origin main


