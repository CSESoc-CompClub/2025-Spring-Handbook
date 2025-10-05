# Cookies

> [!INFO] What are cookies?
> Cookies are a small piece of data that browsers use to identify you. It allows it to remember information like your browsing history, shopping cart items, whether you were logged in or not, and site preferences, and are not neccesarrily bad.

### Cookies can sometimes store a special kind of token (JWT tokens), like a special id that is used for authentication. If you could somehow trick the computer to think you are someone else, then you could gain access to their account.

### There are 3 main parts of a JWT.

#### Each JWT can be split into 3 main parts.

1. Header
   - Contains metadata.
   - The type of the JWT token.
2. Payload
   - The main user data that is being sent.
   - Contains certain key-value pairs, like 'isadmin': true
3. Signature
   - The 'password' that is being sent with the token, that is used to verify that the token hasn't been modified.

> [!INFO] How to decode a cookie?
> Say we have a token like `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6ImNvbnJhZCIsImlhdCI6MTc1OTU4MTk1NywiZXhwIjoxNzU5NTg1NTU3fQ.RUjnxcJ_NhGWGqeEQvisgzF5jeRgL7o1ROynocUX-c0`

> 1. First, paste the token into the token field in [this decoding tool](https://fusionauth.io/dev-tools/jwt-decoder)
> 2. Modify the payload. Notice how the entire token changes even with a very small change.
> 3. Copy the changed token and paste it back into the browser. (Right click, Inspect, Storage, Cookies, and click on the value field of the token. )

> [!SUCCESS] Tasks
>
> 1. The tasks for this activity is to exploit this to gain access to a user profile on the pirate website.
> 2. How might we use the steps above to help us?
