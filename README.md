# YelenImport

Backend API for **YelenImport**, an e-commerce platform for imported products, built with **FastAPI**, **SQLAlchemy** and **PostgreSQL**.

## Features

- User registration and JWT authentication (OAuth2 password flow)
- Product catalogue
- Shopping cart
- Orders
- Favourites / wishlist
- User management

## Tech stack

| Layer | Tools |
|---|---|
| Framework | FastAPI, Uvicorn |
| Database | PostgreSQL, SQLAlchemy, psycopg2 |
| Validation & config | Pydantic, pydantic-settings, python-dotenv |
| Auth | python-jose (JWT), passlib (bcrypt) |

## Project structure

```
backend/
├── app/
│   ├── core/          # settings and security helpers
│   ├── db/            # database session and base
│   ├── dependencies/  # shared FastAPI dependencies
│   ├── models/        # SQLAlchemy models
│   ├── routers/       # auth, cart, orders, favourites, users
│   ├── schemas/       # Pydantic schemas
│   ├── services/      # business logic
│   └── main.py        # app entry point
├── tests/
└── requirements.txt
```

## Getting started

```bash
git clone https://github.com/almondweisley/YelenImport.git
cd YelenImport/backend

python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

pip install -r requirements.txt
```

Create a `.env` file in `backend/` with your database URL and JWT secret, then run:

```bash
uvicorn app.main:app --reload
```

Interactive API docs will be available at http://localhost:8000/docs.

## Authors

- [@almondweisley](https://github.com/almondweisley)
- [@weisleydan](https://github.com/weisleydan)
