
# Flask and Heroku

I am preparing for a new project, and am testing out the Flask framework.
Additionally, I am becoming more comfortable with hosting via Heroku.

First, I followed this tutorial: https://www.geeksforgeeks.org/deploy-python-flask-app-on-heroku/.

As I go forward I am experimenting with Flask and Heroku some more.

---

## What I Know so Far

### Deploying the App

- To run locally, run `app/main.py`. In VSCode this can be done with `F5`.

- To push to the Heroku servers, simply push to the personal repository. On
  Heroku, I set it up to immediately run the version that is pushed to the main
  branch (if it passes CI, which is not yet set up).

- The site is https://eflask-app-067.herokuapp.com/, and it runs indefinitely.

### Files

- The file `.gitignore` instructs git to ignore certain files, such as 
  `__pycache__` folders which are generated by python to store some information.

- The files `Pipfile` and `Pipfile.lock` were generated through the `pipenv` 
  command, and appear to give information on dependencies and the environment.

- The file `Procfile` appears to tell the server what to run on startup; 
  specifically, it runs `gunicorn` and targets the app variable in `app/main.py`.

- The file `runtime.txt` is used by Heroku. It contains info regarding which
  version of Python to use. Only some are available, and the one reccomended by
  the tutorial does not work.

- The file `wsgi.py` (alternatively, `app.py`) is the starting point for code 
  execution.

- The folder `app` will contain code for the server to use, and resources like 
  HTML, CSS, and images that are sent.
