# automate-google-search-using-python
google custome api python script to search and reture bulk url/domains title and link

1.Create Google API Key
https://developers.google.com/

2.create google search engine
https://programmablesearchengine.google.com/controlpanel/all

3.Install the Google client library
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib

from apiclient.discovery import build
import openpyxl

api_key = "XXXXXXXXXXXXXXXX"

resource = build("customsearch", 'v1', developerKey=api_key).cse()
path = "C:\\Users\\url.xlsx"
wb_obj = openpyxl.load_workbook(path)
sheet_obj = wb_obj.active
m_row = sheet_obj.max_row
m = "malware"
for i in range(1, m_row + 1):
	k = sheet_obj.cell(row = i, column = 1)
	m = "('malware' OR 'virus' OR 'adware' OR 'exploit' OR 'vulnerabilities')"
	z = k.value 
	x= z + m
	
	print(z)
	result = resource.list(q=x, cx='03b7e7f18d0184522').execute()
	for item in result['items']:
		print(item['title'], item['link'])
		
