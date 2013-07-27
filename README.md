Simple Google App Engine Application
====================================
Migrated from Python 2.5 to Python 2.7

Replace the WSGI CGI handler => 
                script: django_bootstrap.application 
        instead of 
                script: django_bootstrap.py


Update indexes
clean index.yaml
 appcfg.py update_indexes gifts-test

Python 2.7 configuration requires third-party libraries specified in app.yaml:

libraries:
- name: django
  version: "1.3"
  
google.appengine.dist and djangoforms are no longer supported
  
Authentication Type should be set properly in Application Settings, otherwise expect:  
    Exception Type:	NotAllowedError
    Exception Location:	/../appengine/api/users.py in create_login_url, line 256