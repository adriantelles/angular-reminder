# Reminder
Reminder is a simple tool to keep task/notes with markdown, also work as  a CMS to manage documents/attachments.  

This web app is created with Angular and Flask. 

To start this app, please follow below steps.


## Env Setup 

1. Install Python27
2. Navigate to the root folder with `cd Reminder`
3. run `pip install -r python_requirements.txt` 
4. run `npm install`
5. run `bower install`


## Start app

1. Before start the app, please create the db first:

	- Navigate to the db utils folder with `cd db_utils`
	- run `python db_create.py` 
	- run `python db_migrate.py`
	
2. Run default gulp task to import related JavaScript lib from bower folder:

	- run `gulp`

3. Start the app:

	- Navigate to the root folder with `cd Reminder`
	- run `python run.py`

4. Now visit http://localhost:5000/


## Misc

1. Python style check with pylint

    - `pylint --rcfile=pylint.conf app` 

2. JavaScript style check with jshint

    - `gulp jshint`     
    
3. Run JavaScript unit test

    - `karma start`
    - check the test coverage at "Reminder\TestFiles\coverage\" folder
    
4. Some atomic gulp tasks under "Reminder\gulp_tasks\atomic_tasks\"    

5. Set `app.debug = True` to `False` in "Reminder\app\__init__.py" to disable debug mode

    - In non-debug mode, Flask will leverage minified HTML/CSS/JS to reduce HTTP request number/size
    - Minified HTML/CSS/JS were saved in "Reminder\app\build\templates" and "Reminder\app\build\static" 
