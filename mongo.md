---
title: Databases
---
[< Back to index](index.md)

## MongoDB

### Python Code
```Python
import json
import pprint
from bson import json_util
from pymongo import MongoClient

connection = MongoClient('localhost', 27017)
db = connection['city']
collection = db['inspections']

def read():
    try:
        userKey = raw_input('Enter key field: ')
        userValue = raw_input('Enter value for key field: ')
        oneOrMany = raw_input('\nSelect 1 to find the first record that matches, \nSelect 2 to find up to 10 records that match\n')
    
    except ValidationError as ve:
        abort(400, str(ve))
        
    try:
        if oneOrMany == '1':
            pprint.pprint(collection.find_one({ userKey : userValue}))
        elif oneOrMany == '2':
            return10 = collection.find({userKey : userValue}).limit(10)

            for document in return10:
                pprint.pprint(document)
    
    except ValidationError as ve:
        abort(400, str(ve))

def main():
    read()
    
main()
```
### Sample Output


[< Back to index](index.md)
