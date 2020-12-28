# Worldbank Dashboard Udacity

Data visualization dashboard built using Flask, Bootstrap and Plotly. This project is part of Udacity's data science Nanodegree.

Following the instructions below will launch data vis dashboard showing charts using world bank data.

View the dashboard [here](https://world-bank-dash.herokuapp.com/).

## Requirements

In terminal do to directory and use the package manager [pip](https://pip.pypa.io/en/stable/) to install requirements.

```bash
cd world-bank-dash
pip install -r requirements.txt
```

## Usage
Run local server

Add the line ```app.run(host='0.0.0.0', port=3001, debug=True)``` to worldbank.py to test. Run worldbank.py in your shell.

```bash
python worldbank.py
```
In your browser go to http://localhost:3001 to view site.

## Heroku setup as provided by Udacity

Make sure that the web app is working locally.

2. Next, go to www.heroku.com and create an account if you haven't already.

3. Then, follow the process given in the previous video:
- update python using the terminal command `conda update python`

- create a virtual environment. Note that you can create the virtual environment inside the 5_deploy folder. But then you would end up uploading that folder to Heroku unecessarily. Consider creating the virtual environment in the workspace folder. Or alternatively, you can create a .gitignore file inside the 5_deploy folder so that the virtual enviornment folder gets ignored

- pip install the libraries needed for the web app. In this case those are flask, pandas, plotly, and gunicorn.

- next install the heroku command line tools with the following command:

```bash
curl https://cli-assets.heroku.com/install-ubuntu.sh | sh
https://devcenter.heroku.com/articles/heroku-cli#standalone-installation
```

- then check the installation with the command:

```bash
heroku —-version
```

- next, log into heroku using the command:
```bash
heroku login
```
and then enter your email and password when asked

- remove ```app.run()``` from the worldbank.py file

- cd to root directory and create a procfile with the command
```
touch Procfile
```
and put the following in the Procfile
```
web gunicorn worldbank:app
```

- Then create a requirements file with this command:
pip freeze > requirements.txt

- Next, initialize a git repository with the following commands:
```
git init
git add .
```

- configure the email and user name, you can use these commands:
```
git config --global user.email email@example.com
git config --global user.name "my name"
```

- make a commit with this command:
```
git commit -m "first commit"
```

- create a uniquely named heroku app. Use this command:
```
heroku create my-app-name
```
If you get a message that the app name is already taken, try again with a different app name until you find one that is not taken

- check that heroku added a remote repository with this command:
```
git remote -v
```

- push the app to Heroku:
```
git push heroku master
```

Go to the link for your web app to see if it's working. The link should be https://app-name.heroku.com

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
