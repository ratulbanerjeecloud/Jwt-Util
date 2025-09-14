# Jwt-Util

Reusable Java library for JWT token generation and validation using JJWT.

## Features
- Generate JWT tokens with subject, issued date, and expiration
- Validate JWT tokens
- Extract subject from JWT tokens

## Usage
Add this JAR as a dependency in your microservices. Example:

```java
JwtTokenUtil jwtUtil = new JwtTokenUtil("your-256-bit-secret", 3600000); // 1 hour expiry
String token = jwtUtil.generateToken("user@example.com");
boolean valid = jwtUtil.validateToken(token);
String subject = jwtUtil.getSubjectFromToken(token);
```

## Configuration
- Use a secure 256-bit secret key for production
- Set token expiration as needed

## Dependencies
- JJWT 0.12.3

---
Replace the secret key with a secure value in production.