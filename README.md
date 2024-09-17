# interview

1. route guards
2. canActivate
3. canLoad
4. loadChildren
5. forkJoin: handle multiple observables for the 1st one 1 second, and the 2nd one 5 seconds.
6. merge
7. authentication an authorization
8. method overloading and method overiding
9. observables
10. 

# Angular Project Security Best Practices

This guide outlines the best practices for improving security in an Angular project. Following these practices can help mitigate common security risks and enhance the protection of your application.

## Table of Contents

- [1. Enable Content Security Policy (CSP)](#1-enable-content-security-policy-csp)
- [2. Use Angular’s Built-in Security Features](#2-use-angulars-built-in-security-features)
- [3. Avoid Direct DOM Manipulation](#3-avoid-direct-dom-manipulation)
- [4. Use HTTPS](#4-use-https)
- [5. Implement Authentication and Authorization](#5-implement-authentication-and-authorization)
- [6. Sanitize User Inputs](#6-sanitize-user-inputs)
- [7. Use Angular's HttpClient Module](#7-use-angulars-httpclient-module)
- [8. Disable Debug Tools in Production](#8-disable-debug-tools-in-production)
- [9. Limit Exposure of Data](#9-limit-exposure-of-data)
- [10. Keep Dependencies Updated](#10-keep-dependencies-updated)
- [11. Use Environment-specific Configurations](#11-use-environment-specific-configurations)
- [12. Strict CORS Policies](#12-strict-cors-policies)
- [13. Audit and Monitor](#13-audit-and-monitor)

## 1. Enable Content Security Policy (CSP)

CSP is a security measure that helps mitigate cross-site scripting (XSS) and data injection attacks by defining which resources are allowed to be loaded by the browser.

- **Example:** Configure a CSP that allows only trusted sources (e.g., your own domain or trusted CDNs).
- **Implementation:**
  ```html
  <meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self' https://trusted-cdn.com;">

