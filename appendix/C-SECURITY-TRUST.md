# Appendix C — Security & Trust Checklist

> *Security is the control room for protecting what is now worth something. It is not a luxury. It is the floor beneath everything else.*

This checklist addresses the Trust Control Room — the defensive surface of the empire. It is not exhaustive, but it covers the baseline posture that a platform handling user data and transactions must demonstrate.

---

## Section 1: Authentication & Access

- [ ] User passwords are hashed with a modern algorithm (bcrypt, argon2, or equivalent)
- [ ] Password reset flow does not expose sensitive data in URLs or emails
- [ ] Admin/operator access is protected with strong credentials and, ideally, MFA
- [ ] There is no default or shared credential in use anywhere in the system
- [ ] Session tokens are invalidated on logout

---

## Section 2: Data Handling

- [ ] Personally identifiable information (PII) is identified in the data model
- [ ] PII is stored with appropriate access controls — not exposed in logs or public API responses
- [ ] Payment data is handled via a compliant payment provider (PCI scope is minimized)
- [ ] The platform knows where user data lives and can delete it on request
- [ ] Data retention policy is defined (even informally)

---

## Section 3: Platform Integrity

- [ ] Dependencies (packages, libraries, services) are at reasonably current versions
- [ ] No known high/critical CVEs exist in current dependencies (check regularly)
- [ ] User-generated content (listings, images, text) is sanitized before storage and display
- [ ] File upload handling (if applicable) restricts file types and validates content
- [ ] SQL queries or ORM interactions are protected against injection

---

## Section 4: Transport Security

- [ ] All platform surfaces are served over HTTPS
- [ ] HTTPS certificates are valid and auto-renewed
- [ ] HTTP traffic redirects to HTTPS
- [ ] Security headers are in place (CSP, X-Frame-Options, HSTS at minimum)

---

## Section 5: Monitoring & Response

- [ ] Error logging is in place and reviewed regularly
- [ ] Unusual activity patterns (login failures, scraping, abuse) can be detected
- [ ] A process exists for responding to a reported vulnerability or breach
- [ ] The operator has a contact email published for security reports

---

## Section 6: Trust Signals to Users

- [ ] Privacy policy is published, current, and accurate
- [ ] Terms of service are published and cover the platform's actual use cases
- [ ] Cookie consent mechanism is in place (if applicable by jurisdiction)
- [ ] Trust-building elements exist on the platform (verified badges, review systems, or equivalent for the vertical)

---

*Review this checklist before any significant marketing push or partnership announcement. Trust is easier to build than to rebuild.*
