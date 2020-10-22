# WorkIndia-TodoApp
An API application that can create a list of todos for secret agents and display all todos of a agent by due date first. It also has hashing for security of credential as all agents needs it ;)

## Requirements
PHP, mySQL

### Agent account registration:
Create a agent account. These credentials will be used to log into this panel.

[POST] /app/agent

Request Data: {
    'username': str,
    'password': str
}

Response Data: {
    'status': 'account created'
    'status_code':200
}

### Agent account login:
[POST] /app/agent/auth

Request Data: {
    'agent_id': int,
    'password': str
}

#### For success:

Response Data: {
    'status': 'success',
    'agent_id': int,
    'status_code': 200
}

#### For failure:

Response Data: {
    'status': 'failure',
    'status_code': 401
}

### Task todo list:

[GET] /app/sites/list/?agent={agentId}

Request Data: None

Response Data: [list of TODO items with their details]

### Post Agent new tasks:

[POST] /app/sites?agent={agentId}

Request Data: {
    'title': str,
    'description': str,
    'category': str,
    'due_date': date
}
Response Data: {
    'status': 'success',
    'status_code': 200
}

## Thank you for Checking my assignment out :)
