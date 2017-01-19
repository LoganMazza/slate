# Errors

<aside class="notice">This error section is stored in `includes/_errors.md`.</aside>

The EchidnAPI uses these error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- Your request is bad and you should feel bad
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- The echidna requested is burrowed. Administrators only
404 | Not Found -- The specified echidna could not be found
405 | Method Not Allowed -- You tried to access an echidna with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
410 | Gone -- The echidna requested has been removed from our servers
418 | How are they mammals?
429 | Too Many Requests -- You're requesting too many echidnas! Slow down!
500 | Internal Server Error -- There is a problem with our server. Try again later.
503 | Service Unavailable -- The server is temporarially offline for maintanance. Please try again later.
