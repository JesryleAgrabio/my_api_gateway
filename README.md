Setup Instructions

Install XAMPP if you haven't already.
Copy the entire my_api_gateway/ folder into your htdocs/ directory (e.g., C:\xampp\htdocs\my_api_gateway).
Start Apache and MySQL from the XAMPP Control Panel.
Create a MySQL database use the apigatewaydb.sql Copy and Paste it.
Valid API Keys Implemented image

How to test features (POSTMAN/ CURL) Remember: You must always include the header X-API-Key when making requests.

Accessing /users Service. •Method: GET •URL: http://localhost:8080/my_api_gateway/api/users •Headers: •X-API-Key: key123 •X-API-Key: key456 ![image](https://github.com/user-attachments/assets/51038fa5-67c5-4195-9f64-93998bac6ca5)

Accessing /products Service. •Method: GET •URL: http://localhost:8080/my_api_gateway/api/products •Headers: •X-API-Key: key123 •X-API-Key: key456 ![image](https://github.com/user-attachments/assets/89ee0595-5533-4f94-a6a9-4bf3590f28a1)

Accessing /dashboard Service. •Method: GET •URL: http://localhost:8080/my_api_gateway/api/dashboard •Headers: •X-API-Key: key123 •X-API-Key: key456 ![image](https://github.com/user-attachments/assets/e5f32b8d-669c-4696-9a5c-a411b86a76d0)


Challenges Faced / Assumptions Made 
Challenge: Implementing a dynamic rate limiting has been hard with db. 
Assumption: Every API key inputted in the databases is valid until it is removed manually from the db.  

Unauthorized User: ![image](https://github.com/user-attachments/assets/4728a0ee-ddaa-4798-8abc-d71aa6c9cd75)

Rate Limiter: ![image](https://github.com/user-attachments/assets/2e4e3060-b31e-4bc9-97ec-82cbe47362f0)


Gateway Logs: ![image](https://github.com/user-attachments/assets/dd8cf354-22d6-45df-a9e8-a21ebe595d0b)

