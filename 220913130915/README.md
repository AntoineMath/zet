# How JWT works?  

## JSON Web Token
A JWT has 3 parts:
1. Header: represents token type algo used for signin and encoding.
2. Payload: **Do not put sensitive informations in it**
3. Signature: calculated by encoding and concatanating the header and payload. It is then passed to the cryptographic algo.  
```
data = base64urlEncode( header ) + "." + base64urlEncode( payload )
signature = HMAC-SHA256( data, secret_salt )
```

## Steps
1. User signin, server returns JWT
2. GET/protected-resource (with Bearer JWT)
3. Hash the JWT token with the server private key and detect if it's the same as the one sent.




## References
    https://dev.to/kcdchennai/how-jwt-json-web-token-authentication-works-21e7#:~:text=Authentication%20server%20verifies%20the%20credentials,the%20secret%20salt%2F%20public%20key.
