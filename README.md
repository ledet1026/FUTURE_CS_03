# FUTURE_CS_03
# JSONPlaceholder API Security Analysis

## Overview
This repository contains a security assessment of the **JSONPlaceholder** public REST API.  
The analysis identifies common API vulnerabilities, including:

- Excessive data exposure  
- Unauthenticated access  
- Broken object-level access (IDOR)  
- Missing or weak rate limiting  
- Insufficient input validation  

Testing was performed manually using **Postman**.

---

## Scope
- **Endpoints Tested:** `/users`, `/users/1`, `/posts`, `/posts/1`, `/posts?userId=1`, `/comments`, `/todos`  
- **Tools Used:** Postman, Browser Developer Tools  
- **Focus:** Data exposure, authentication, authorization, input validation, rate limiting  

---

## Key Findings
- Sensitive data exposed without restrictions  
- Endpoints accessible without authentication  
- Predictable IDs allow unauthorized access (IDOR)  
- Unlimited requests possible (no rate limiting)  
- Query parameters not validated properly  

**Risk Severity:** Medium (1–3), Low (4–5)  

---

## Recommendations
- Enforce authentication and authorization  
- Implement object-level access control  
- Apply input validation and correct data types/formats  
- Use rate-limiting to prevent abuse  
- Limit exposure of sensitive fields  
