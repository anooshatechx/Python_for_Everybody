# Python for Everybody - Course 3 Notes
‎
## 1.Web Scraping & Parsing

‎- Extract information from webpages automatically.
‎

### For Fetching Data:

‎- *urllib* (gets the data from HTML)
```python
‎from urllib.request import urlopen
‎html = urlopen(url).read()
```

### For Parsing Data:

‎- *BeautifulSoup* (built-in library) (parses HTML & extract data)
```python
‎from bs4 import BeautifulSoup
‎soup = BeautifulSoup(html,"html.parse")
```

### Steps:

‎1. Import libraries
‎2. Request webpage  
‎3. Open & Read the webpage
‎4. Parse HTML  
‎5. Extract tags/text (what you need)
‎

### Basic Example:

```python
‎from urllib.request import urlopen
‎from bs4 import BeautifulSoup
‎
‎url = "http://example.com"
‎html = urllib.request.urlopen(url).read()
‎soup = BeautifulSoup(html, "html.parser")
‎
‎for tag in soup('a'):
‎    print(tag.get('href',None))
```
‎

### HTML tags:
‎- a & href are fixed by HTML rules
‎- a is anchor tags
- href is where url links are stored
‎
‎
‎---
‎
## 2.JSON
‎
‎-Most APIs return data in JSON.
‎

### ‎JSON to Python:
```python
‎import json
‎data = '{"name":"Anoosha"}'
‎info = json.loads(data)
```
‎

### Python to  JSON:
```python
‎json.dumps({'a': 10, 'b': 20})
```
‎
‎
### JSON from URL:
```python
response = urlopen(url).read()
‎info = json.loads(response)
```

‎‎---
‎
### ‎3.APIs
‎
‎-A service that gives you data when you request it.
‎

### ‎Steps:
‎
‎1. API URL and Parameters
‎2. Send request
‎3. API returns JSON
‎4. Parse it
‎5. Print the data you want
‎
### ‎Example

```python
‎import requests
‎import json
‎
‎service = "https://maps.googleapis.com/maps/api/geocode/json"
‎param = {'address': 'New York', 'key': 'YOUR_API_KEY'}
‎extract = requests.get(service,params=param)
‎
‎info = extract.json()
‎
‎*where exactly it is that you wanna extract*
‎print(json.dumps(info,indent=4))
‎
‎print(info)
```


### Key Terms:
‎
‎1. Endpoint (API URL)
‎2. Parameters (Extra info (like address=…))
‎3. API Key (Your access password)
‎4. Response (JSON from the server)
‎
‎
‎‎---
‎

## 🎯 Summary
‎
**‎Web Scraping**: Extract HTML data
‎
‎**JSON**: Format for sending & receiving data
‎
**APIs**: Get real online data using Python
‎
‎
