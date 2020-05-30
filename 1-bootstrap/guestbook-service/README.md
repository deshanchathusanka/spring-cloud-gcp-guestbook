Package command : \
mvnw clean package \

Run command : \
Method 1 : mvnw -q spring-boot:run -Dserver.port=8081 \
Method 2 : \
Step 1 (Build) : mvnw clean package \
Step 2 : java -jar target/guestbook-0.0.1-SNAPSHOT.jar \

Get request : \
curl -s http://localhost:8081/guestbookMessages \

POST request : \
curl -XPOST -H "content-type: application/json" \
  -d '{"name": "Ray", "message": "Hello"}' \
  http://localhost:8081/guestbookMessages \
  
  
  
Retrieve all available REST endpoints : \
curl http://localhost:8081 \

Retrieve all customer records (select all query): \
curl http://localhost:8081/customer \

Insert customer record : \
curl -i -H "Content-Type:application/json" -d "{\"firstName\":\"Deshan\",\"lastName\":\"Chathusanka\",\"address\":\"ambalantota\"}" http://localhost:8081/customer \

Find all custom queries \
curl http://localhost:8081/customer/search \

Select customers using last name (custom query): \
curl http://localhost:8081/customer/search/findByLastName?lastName=Chathusanka \