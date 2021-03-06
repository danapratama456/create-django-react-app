# create-django-react-app
A simple script to create a Django-backed React app, all in one.

# Install via PyPi
`pip install create-django-react-app`

# Credit
This script is based almost 100% on this walkthrough:
https://medium.com/@dakota.lillie/django-react-jwt-authentication-5015ee00ef9a

The only difference is adding the React app to the project instead of needing a separate front end.  You then just need to set your webserver to serve the app build folder as static, and you're good to go.

# What it Does
This script creates a Django project, creates a React app within in (in the /app directory) and then adds basic JWT code to enable login, logout, and signup.  

# How to use
Requirements: Python and Node must already be installed.
Side effects: This will install Django and pipenv globally.

1. Install via PyPi: `pip install create-django-react-app` 
2. Run `create-django-react-app name-of-project`
3. The script then runs through installing all needed dependencies and files.

# How this setup works
In development:
You can run the django development server and the react development server simultaneously to test the app during development.

In production:
1. Build your react app in place. `npm run build`
2. Host your Django app using your preferred solution.
3. Map a static path `/app/` to the build folder. `/app/build/` 

I use PythonAnywhere, which makes this setup very easy to use, but you should be able to adapt this to other server configurations/solutions.
