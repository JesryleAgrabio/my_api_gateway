Setup Instructions

Install XAMPP if you haven't already.
Copy the entire my_api_gateway/ folder into your htdocs/ directory (e.g., C:\xampp\htdocs\my_api_gateway).
Start Apache and MySQL from the XAMPP Control Panel.
Create a MySQL database use the apigatewaydb.sql.
Valid API Keys Implemented image

How to test features (POSTMAN/ CURL) Remember: You must always include the header X-API-Key when making requests.

Accessing /users Service. •Method: GET •URL: http://localhost:8080/my_api_gateway/api/users •Headers: •X-API-Key: key123 •X-API-Key: key456 image
2.Accessing /products Service. •Method: GET •URL: http://localhost:8080/my_api_gateway/api/products •Headers: •X-API-Key: key123 •X-API-Key: key456 image

Challenges Faced / Assumptions Made Challenge: Implementing dynamic rate-limiting for each API key without using external libraries. Assumption: Every API key is valid indefinitely unless manually removed from the database. Assumption: Rate limits are set as 10 requests per minute per API key. Challenge: Handling header retrieval uniformly because different environments (like Apache vs. Nginx) can behave differently with getallheaders().

Unauthorized User: image

Rate Limiter: image

Gateway Logs: image
