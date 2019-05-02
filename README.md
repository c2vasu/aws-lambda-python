# aws-lambda-python

- virtualenv
```
pip install virtualenv --user
```
- cd aws-lambda-python
```
cd aws-lambda-python
```

- create env
```
python -m virtualenv .
```
- activate
```
source bin/activate
```
- install custom packages
```
pip install bs4 --user
```
- create lambda fuction
```
touch lib/python2.7/site-packages/lambda_function.py
```
- add code snippet
```
import json
import bs4

def lambda_handler(event, context):
    # TODO implement
    return {
        'statusCode': 200,
        'body': json.dumps('Hello from Lambda!')
    }
```
- Zip folder (lib/python2.7/site-packages) and upload to aws lambda
```
zip -r9 ../function.zip .
```
- update lambda fuction
```
cd ..

aws lambda update-function-code --function-name aws-lambda-python --zip-file fileb://function.zip
```





