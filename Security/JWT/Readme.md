# JWT 

JSON Web Tokens (JWTs) are a standardized way to securely transmit information between parties as a JSON object. They are widely used in authentication and authorization processes. 
They contain JSON objects which have the information that needs to be shared. Each JWT is also signed using cryptography (hashing) to ensure that the JSON contents cannot be affected by the malicious party.
When respone is send from auth server there is no way that API's can verify the authenticity of the data. Due to this, the auth server needs to transmit this information in a way that can be verified by the client application, and this is where the concept of a TOKEN comes into the picture. 

### Token 

A token is a string that contains some information that can be verified securely. It could be a random set of alphanumeric characters which point to an ID in the database, or it could be an encoded JSON that can be self-verified

![](img/TOKEN_STRUCT.png)

This token generally consists of 3 parts  

1) Header: Consists of two parts:  
    a)The signing algorithm that’s being used.  
    b)The type of token, which, in this case, is mostly “JWT”.  
2) Payload: The payload contains the claims or the JSON object.
3) Signature: A string that is generated via a cryptographic algorithm that can be used to verify the integrity of the JSON payload.

When the server gets the information from the client they are going to decode the Header and Payload using the algorithm specified in the header 
and the secret key. This decoded part is then compared with the Signature to check whether the user is authorized. 
