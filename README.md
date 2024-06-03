Exception in thread django-main-thread:
Traceback (most recent call last):
  File "/usr/lib/python3.10/threading.py", line 1016, in _bootstrap_inner
    self.run()
  File "/usr/lib/python3.10/threading.py", line 953, in run
    self._target(*self._args, **self._kwargs)
  File "/home/sasho/.local/lib/python3.10/site-packages/django/utils/autoreload.py", line 64, in wrapper
    fn(*args, **kwargs)
  File "/home/sasho/.local/lib/python3.10/site-packages/django/core/management/commands/runserver.py", line 133, in inner_run
    self.check(display_num_errors=True)
  File "/home/sasho/.local/lib/python3.10/site-packages/django/core/management/base.py", line 486, in check
    all_issues = checks.run_checks(
  File "/home/sasho/.local/lib/python3.10/site-packages/django/core/checks/registry.py", line 88, in run_checks
    new_errors = check(app_configs=app_configs, databases=databases)
  File "/home/sasho/.local/lib/python3.10/site-packages/django/core/checks/urls.py", line 14, in check_url_config
    return check_resolver(resolver)
  File "/home/sasho/.local/lib/python3.10/site-packages/django/core/checks/urls.py", line 24, in check_resolver
    return check_method()
  File "/home/sasho/.local/lib/python3.10/site-packages/django/urls/resolvers.py", line 519, in check
    for pattern in self.url_patterns:
  File "/home/sasho/.local/lib/python3.10/site-packages/django/utils/functional.py", line 47, in __get__
    res = instance.__dict__[self.name] = self.func(instance)
  File "/home/sasho/.local/lib/python3.10/site-packages/django/urls/resolvers.py", line 738, in url_patterns
    patterns = getattr(self.urlconf_module, "urlpatterns", self.urlconf_module)
  File "/home/sasho/.local/lib/python3.10/site-packages/django/utils/functional.py", line 47, in __get__
    res = instance.__dict__[self.name] = self.func(instance)
  File "/home/sasho/.local/lib/python3.10/site-packages/django/urls/resolvers.py", line 731, in urlconf_module
    return import_module(self.urlconf_name)
  File "/usr/lib/python3.10/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "<frozen importlib._bootstrap>", line 1050, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1027, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1006, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 688, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 883, in exec_module
  File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
  File "/home/sasho/dev/puddle/puddle/puddle/urls.py", line 8, in <module>
    path('', include('core.urls')),
  File "/home/sasho/.local/lib/python3.10/site-packages/django/urls/conf.py", line 39, in include
    urlconf_module = import_module(urlconf_module)
  File "/usr/lib/python3.10/importlib/__init__.py", line 126, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
  File "<frozen importlib._bootstrap>", line 1050, in _gcd_import
  File "<frozen importlib._bootstrap>", line 1027, in _find_and_load
  File "<frozen importlib._bootstrap>", line 1006, in _find_and_load_unlocked
  File "<frozen importlib._bootstrap>", line 688, in _load_unlocked
  File "<frozen importlib._bootstrap_external>", line 883, in exec_module
  File "<frozen importlib._bootstrap>", line 241, in _call_with_frames_removed
  File "/home/sasho/dev/puddle/puddle/core/urls.py", line 3, in <module>
    from . import views
  File "/home/sasho/dev/puddle/puddle/core/views.py", line 19
    from = SignupFrom()
         ^
SyntaxError: invalid syntax


from django import froms
from django.contrib.auth.form import UserCreationFrom
from django.contrib.auth.models import User

class SignupFrom(UserCreationFrom):
    class Meta:
        model = User
        fields = ('username', 'email', 'password1', 'password2')


        from django.shortcuts import render

from item.models import Category, Item

from .forms import SignupFrom

def index(request):
    items = Item.objects.filter(is_sold=False) [0:6]
    categories = Category.objects.all()
    return render(request, 'core/index.html', {
        'categories': categories,
        'items': items,
    })

def contact(request):
    return render(request, 'core/contact.html')

def signup(request):
    from = SignupFrom()

return render(request, 'core/signup.html',{

})
