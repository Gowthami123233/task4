Requirements
requests>=2.31.0,<3.0.0
beautifulsoup4>=4.12.0,<5.0.0

Flask>=2.3,<3.0


# Flask User REST API

A minimal Flask REST API to manage users in memory. Includes GET, POST, PUT, and DELETE endpoints.

## Requirements
- Python 3.9+ (Windows `py -3` works fine)
- Dependencies listed in `requirements.txt`

## Install
```powershell
py -3 -m pip install -r requirements.txt
```

If `py -3` is unavailable, use:
```powershell
python -m pip install -r requirements.txt
```

## Run
```powershell
py -3 api.py
```
The server will start at `http://127.0.0.1:5000`.

## Endpoints
- GET `/users` — list all users
- GET `/users/{id}` — get a single user
- POST `/users` — create a user
- PUT `/users/{id}` — update a user (partial or full)
- DELETE `/users/{id}` — delete a user

### Request/Response Examples (PowerShell)

Create:
```powershell
curl -Method POST -Uri http://127.0.0.1:5000/users -ContentType 'application/json' -Body '{"name":"Alice","email":"alice@example.com","age":30}'
```

List:
```powershell
curl http://127.0.0.1:5000/users
```

Get by id:
```powershell
curl http://127.0.0.1:5000/users/1
```

Update:
```powershell
curl -Method PUT -Uri http://127.0.0.1:5000/users/1 -ContentType 'application/json' -Body '{"age":31}'
```

Delete:
```powershell
curl -Method DELETE -Uri http://127.0.0.1:5000/users/1
```

## Notes
- Data is stored in memory and resets when the server restarts.
- Required fields to create a user: `name`, `email`; optional: integer `age`.

## Push to GitHub (PowerShell)
```powershell
git init
git add .
git commit -m "Add Flask user REST API"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```
```
