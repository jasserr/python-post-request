#requests is a python library for sending requests to sites
#hashlib is a library to convert the string provived to md5
#BeautifulSOup is a python library to parse HTML data .

import requests, hashlib 

from bs4 import BeautifulSoup 

url="http://167.99.85.197:30144/"

s = requests.session() #Creating a session
response= s.get(url) #getting a response from our webpage  

soup = BeautifulSoup(response.content, "lxml")  #contains the content of the webpage


str=soup.h3.string #getting the given string from the url with it's header which is H3

hash = hashlib.md5(str.encode()).hexdigest() #ecrypting hash 

obj={'hash': hash } #making our data object that contains the hash


r = s.post(url,data= obj) #sending the POST requests
 
print(r.text) #printing the response in text format
