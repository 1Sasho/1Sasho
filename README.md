TemplateDoesNotExist at /signup/
core/signup.html
Request Method:	GET
Request URL:	http://127.0.0.1:8000/signup/
Django Version:	5.0.6
Exception Type:	TemplateDoesNotExist
Exception Value:	
core/signup.html
Exception Location:	/home/sasho/.local/lib/python3.10/site-packages/django/template/loader.py, line 19, in get_template
Raised during:	core.views.signup
Python Executable:	/usr/bin/python3
Python Version:	3.10.12
Python Path:	
['/home/sasho/dev/puddle/puddle',
 '/usr/lib/python310.zip',
 '/usr/lib/python3.10',
 '/usr/lib/python3.10/lib-dynload',
 '/home/sasho/.local/lib/python3.10/site-packages',
 '/usr/local/lib/python3.10/dist-packages',
 '/usr/lib/python3/dist-packages',
 '/usr/lib/python3.10/dist-packages']
Server time:	Mon, 03 Jun 2024 07:45:33 +0000
Template-loader postmortem
Django tried loading these templates, in this order:

Using engine django:

django.template.loaders.app_directories.Loader: /home/sasho/.local/lib/python3.10/site-packages/django/contrib/admin/templates/core/signup.html (Source does not exist)
django.template.loaders.app_directories.Loader: /home/sasho/.local/lib/python3.10/site-packages/django/contrib/auth/templates/core/signup.html (Source does not exist)
django.template.loaders.app_directories.Loader: /home/sasho/dev/puddle/puddle/core/templates/core/signup.html (Source does not exist)
django.template.loaders.app_directories.Loader: /home/sasho/dev/puddle/puddle/item/templates/core/signup.html (Source does not exist)
