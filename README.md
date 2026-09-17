## Planned Microservices

### 1. Authentication and Registration Service

Combines Identity, Authentication, Registration, and Verification.

Responsible for:

- Individual registration
- Organization registration
- OTP generation
- OTP verification
- OTP resend
- Login and logout
- JWT access tokens
- JWT refresh tokens
- Password reset
- User management
- Communication with Organization Service using HTTPX
- Communication with Notification Service using HTTPX

### 2. Organization and Tenant Service

Responsible for:

- Organization creation
- Tenant creation
- Organization domain validation
- Organization activation
- Tenant activation
- Organization and tenant management

### 3. Notification Service

Responsible for:

- Registration OTP emails
- Password reset emails
- Welcome emails
- SMTP or console email delivery
- Notification logs

## Authentication Module Mapping

| Existing Feature | New Microservice |
|---|---|
| User registration | Authentication and Registration Service |
| Organization registration | Authentication and Registration Service + Organization and Tenant Service |
| OTP generation | Authentication and Registration Service |
| OTP verification | Authentication and Registration Service |
| OTP resend | Authentication and Registration Service + Notification Service |
| User login | Authentication and Registration Service |
| User logout | Authentication and Registration Service |
| JWT access token | Authentication and Registration Service |
| JWT refresh token | Authentication and Registration Service |
| Password reset | Authentication and Registration Service + Notification Service |
| User management | Authentication and Registration Service |
| Organization creation | Organization and Tenant Service |
| Tenant creation | Organization and Tenant Service |
| Email notifications | Notification Service |