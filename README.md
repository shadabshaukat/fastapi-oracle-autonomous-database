# fastapi-oracle-autonomous-database

Set the DB_USER, DB_PASSWORD & DB_DSN parameters in the script based on your Autonomous DB

Install the Python3 packages, this has been tested on Python 3.11

pip3 install -r requirements.txt

uvicorn fapi:app --host 127.0.0.1 --port 8001

POST 

curl -X 'POST' \
  'http://localhost:8001/orders/' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
    "order_id": 1,
    "product_name": "Example Product",
    "quantity": 10
  }'

GET

curl -X 'GET' \
  'http://localhost:8001/orders/1' \
  -H 'accept: application/json'
