Run command : mvnw -q spring-boot:run -Dserver.port=8081

Get request : curl -s http://localhost:8081/guestbookMessages

POST request : 
curl -XPOST -H "content-type: application/json" \
  -d '{"name": "Ray", "message": "Hello"}' \
  http://localhost:8081/guestbookMessages