# automate-google-search-using-python
google custome api python script to search and reture bulk url/domains title and link

1.Create Google API Key
https://developers.google.com/

2.create google search engine
https://programmablesearchengine.google.com/controlpanel/all

3.Install the Google client library
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib

if you are facing below error

>> from apiclient.discovery import build
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "C:\Program Files\Python310\lib\site-packages\apiclient\__init__.py", line 8, in <module>
    from googleapiclient import discovery
  File "C:\Program Files\Python310\lib\site-packages\googleapiclient\discovery.py", line 48, in <module>
    import httplib2
  File "C:\Program Files\Python310\lib\site-packages\httplib2\__init__.py", line 52, in <module>
    from . import auth
  File "C:\Program Files\Python310\lib\site-packages\httplib2\auth.py", line 20, in <module>
    auth_param_name = token.copy().setName("auth-param-name").addParseAction(pp.downcaseTokens)
AttributeError: module 'pyparsing' has no attribute 'downcaseTokens'
  
  solution:
  pip install pyparsing==2.4.2
  
  
