# OktaWithSpringSecurity
Okta in Spring Boot implementation with Spring Security and oauth2
Steps : 
1. Create Spring starter project with Dependencies- Spring web & Okta
2. Create Simple Get Mapping to display any message
3. now if you hit API with postman it will not display anything,It will show status : 401 Unauthorized
4. So API will only give respose after authenticate with okta token
5. Authentication Process :
                            in Postman go to Authorization & choose Basic Auth Type & enter username & password (Okta clientId & SecretKey)
                            Go to Body & choose x-www-form-uriencoded
                            KEY : grant_type     VALUE : client_credentials
                            KEY : scope          VALUE : Abhinay (When we go to issuer URL page->Edit option->Add new Scope & named "Abhinay")
   Now Hit API in Postman,We will Get "access Token" in response
6. Now copy access token & hit our "GetMapping" API with Type(Bearer Token) & paste access token there ->Hit Api
7. Now as it is authenticate so we will get Our response which we were expecting
                           
                           

