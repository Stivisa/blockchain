# Simple blockchain example![Opera Snapshot_2025-01-16_153254_docs google com](https://github.com/user-attachments/assets/26b7e34d-d062-4189-a003-4738be88c387)

## Running the Application
To run the application, use the following command:  
```bash
go run main.go
```

# API  endpoints
### 1. Create a New Course

**POST** `http://localhost:3000/new`

Request Body:
```json
{
  "title": "New Course",
  "author": "John",
  "publish_date": "2025-01-08"
}
```
Response:
```json
{
 "id": "5755e4a59c66b669e27138dc745bd7f1",
 "title": "New Course",
 "author": "John",
 "publish_date": "2025-01-08"
}
```
### 2. Checkout course and add block to blockchain

**POST** `http://localhost:3000`

Request Body:
```json
{
 "course_id":"5755e4a59c66b669e27138dc745bd7f1",
 "user":"Anne",
 "checkout_date":"2025-01-16"
}
```
Response:
```json
{
 "course_id": "5755e4a59c66b669e27138dc745bd7f1",
 "user": "Anne",
 "checkout_date": "2025-01-16",
 "is_genesis": false
}
```
### 3. Get whole blockchain

**GET** `http://localhost:3000`
