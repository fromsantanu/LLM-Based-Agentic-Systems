# 📘 Mini-Course: *Understanding `PyJWT` in FastAPI Development*

## **Lesson 1: Introduction to JWT & PyJWT**

* What is a JWT (JSON Web Token)?
* Why JWT is used in FastAPI (authentication, authorization, stateless sessions).
* Structure of JWT (Header, Payload, Signature).
* Installing and importing PyJWT (`pip install PyJWT`).

---

## **Lesson 2: Encoding Tokens with PyJWT**

* Using `jwt.encode(payload, secret, algorithm)`
* Understanding secret keys and algorithms (HS256, RS256).
* Adding expiration (`exp`), issued-at (`iat`), and subject (`sub`) claims.
* Example: generating an access token after user login in FastAPI.

---

## **Lesson 3: Decoding and Verifying Tokens**

* Using `jwt.decode(token, secret, algorithms=[...])`.
* Handling `jwt.ExpiredSignatureError`, `jwt.InvalidTokenError`, etc.
* Demonstrating verification of valid/expired/invalid tokens.
* Example: verifying the token in a FastAPI dependency.

---

## **Lesson 4: Integrating JWT Authentication in FastAPI**

* Creating a dependency to extract the `Authorization: Bearer <token>` header.
* Decoding the token and fetching user info.
* Protecting routes with authentication.
* Example: `get_current_user()` dependency pattern.

---

## **Lesson 5: Refresh Tokens and Expiration Strategy**

* Why access tokens expire quickly.
* Creating and validating refresh tokens.
* Re-issuing access tokens using refresh tokens.
* Example: login route returns both `access_token` and `refresh_token`.

---

## **Lesson 6: Best Practices**

* Keeping the secret key safe (using `.env` file).
* Token expiry and clock skew handling.
* Avoid storing sensitive info inside tokens.
* Using `pydantic` models for token payloads.

---

## **Lesson 7: Advanced Use Cases (Optional)**

* JWT with asymmetric encryption (RS256 public/private keys).
* Using PyJWT with OAuth2PasswordBearer flow.
* Integrating with third-party identity providers.

---


