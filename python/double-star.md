# Double Star in Python

I have seen this before but today I finally bothered to look it up: what does \*\* mean in python?

Well today I learned it can be used in a couple of different ways. To me it seems similar to the spread operator in Javascript. When using it as part of a parameter, such as `**kwargs`, you gain access to the arguments passed in and their keys:

```python
def connect_to_db(**kwargs):
  # kwargs here would look like port=5432, host='localhost'
  port = kwargs['port']
  hostname = kwargs['host']
  # etc etc.
```

You can also use it to pass arguments into a function:

```python
def connect_to_db(port, host):
  # connect

connect_info = dict(port=5432, host='localhost')

connect_to_db(**connect_info)
```

This is called "unpacking", which is how it reminds me of spread. It also works to merge dicts together.

```python
dict1 = {port: 5432, host: 'localhost'}
dict2 = {name: 'my-db', user: 'db-user', password: 'cool-password'}
connect_info = {**dict1, **dict2}
```
