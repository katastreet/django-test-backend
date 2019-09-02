# Install Steps
 * python3 -m venv env
 * source env/bin/activate
 * pip install -r requirements.txt
 * python manage.py migrate
 * python manage.py createsuperuser [ username:test, email:test@gmail.com, password:test]
 * python manage.py runserver
 
 
 # Test steps
 ### Get JWT bearer token
 * localhost:8000/login(POST)
 
 ```
 username: test
 password: test
 ```
 Response(200)
```
 {
    "refresh": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTU2NzUyODYxNSwianRpIjoiMzkxOGQ2MDg0ZDQyNDBjNWFkOTJkYzBiY2Q0NzVhNmYiLCJ1c2VyX2lkIjoxfQ.Enh8j2Ez1kVneIZYYatum0KHv42pKDrMwNmzgwujvLw",
    "access": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNTY3NDQyNTE1LCJqdGkiOiI1YjFmNTFkN2YxZGY0MTRmYWQ1YWZkMDFhYTdhZDNkZSIsInVzZXJfaWQiOjF9.PDpMIuBtuevG8sQZzRYHw3o02Rd7GuOGxU_Cg3lsC1c"
}
``` 
***

 ### Hello endpoint
 * localhost:8000/hello(GET)

*Needs Authentication*
 
 Response(200)
 ```
true
```
 
 
 Frontend repo at: https://github.com/katastreet/react-test-frontend
 
 
