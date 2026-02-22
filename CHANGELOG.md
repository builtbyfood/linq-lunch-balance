# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — 2026-02-21

### Added
- Initial release
- Auth0 Resource Owner Password Credentials (password-realm) grant authentication
- Three-tier smart token caching: cached access token → refresh token → password login
- Weekly schedule (Monday 7:00 AM) with immediate run on deploy
- `sensor.linq_meal_balance` created via Home Assistant REST API
- Sensor attributes: `unit_of_measurement`, `device_class`, `state_class`, `student_name`, `all_accounts`, `last_updated`
- Low-balance push notification (fires once when balance first drops below $10)
- Full error handling for common Auth0 errors: `mfa_required`, `invalid_grant`, `unauthorized_client`
- All credentials stored as Node-RED environment variables — nothing sensitive in the flow JSON
- No custom HA integrations or extra Node-RED modules required
