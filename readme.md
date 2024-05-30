# userinfo

Get randomly-generated user informations on python3!

Usage:
```py
import userinfo
print(userinfo.generate_user())
```

Example output:
```text
{'name': 'Ava Johnson', 'email': 'avajohnson44077@protonmail.com', 'username': 'ava_johnson119', 'password': '2&CY"%bI', 'address': 'Park Ave, Chicago, FL', 'age': 44}
```

Example:
```py
import random
import string
def generate_user():
    user = {}
    user['name'] = generate_name()
    user['email'] = generate_email(user['name'])
    user['username'] = generate_username(user['name'])
    user['password'] = generate_password()
    user['address'] = generate_address()
    user['age'] = generate_age()
    return user
def generate_name():
    first_names = ['John', 'Emma', 'Michael', 'Olivia', 'William', 'Ava', 'Muhammad', 'Artem', 'Johny', 'Taylor', 'Flynn', 'Tyler', 'Arlo']
    last_names = ['Smith', 'Johnson', 'Brown', 'Davis', 'Wilson', 'Debb', 'Swift']
    return random.choice(first_names) + ' ' + random.choice(last_names)
def generate_email(name):
    name = name.lower().replace(' ', '') + str(random.randint(0, 50000))
    domains = ['gmail.com', 'yahoo.com', 'outlook.com', 'hotmail.com', 'proton.me','protonmail.com','defaultmail0.com', 'chex.me', 'chexmail.com', 'chexmail.me', 'business-chex.com', 'business-chexmail.com','business-chexmail.me','business-chex.me']
    return name + '@' + random.choice(domains)
def generate_username(name):
    name = name.lower().replace(' ', '_')
    numbers = ''.join(random.choices(string.digits, k=3))
    return name + numbers
def generate_password():
    characters = string.ascii_letters + string.digits + string.punctuation
    return ''.join(random.choices(characters, k=8))
def generate_address():
    streets = ['Main St', 'Park Ave', 'Oak St', 'Cedar Ln', 'Elm St']
    cities = ['New York City', 'Los Santos', 'Liberty City', 'Los Angeles']
    state = ['CA', 'NY', 'TX', 'IL', 'FL']
    return random.choice(streets) + ', ' + random.choice(cities) + ', ' + random.choice(state)
def generate_age():
    return random.randint(6, 70)
```
Output:
```text
{'name': 'John Swift', 'email': 'johnswift17089@outlook.com', 'username': 'john_swift923', 'password': '["5`Pr#,', 'address': 'Cedar Ln, Los Santos, FL', 'age': 21}
Oak St, Los Angeles, NY
michaelsmith7743@business-chexmail.me
39
Michael Smith
9[/}Dmm^
michael_smith461
```
