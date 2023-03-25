# ADFS RelayState Generator

ADFS Relay State is a parameter used in SAML Implementation to identify a specific resource on a resource provider. For example: To identify an account record in Salesforce.

Relay State specifies the path to which a user would be redirected, once the Identity Provider authenticates the user.

If a user tries to access a specific link embedded in an email such as [https://test-sso-dev-ed.my.salesforce.com/003/o](https://test-sso-dev-ed.my.salesforce.com/003/o) and has already logged in to Salesforce, then the user is redirected to the specific record.

If a user is not authenticated earlier, then user is redirected to the ADFS authentication URL and is authenticated and logged in to Salesforce org. However, in this case user gets redirected to his Salesforce org’s homepage and not the page pointed by embedded link because the redirected URL (with RelayState parameter) did not match ADFS’s expected format. Configuration of ADFS for Relay State and URL encoding can resolve this issue. Using Relay State, you can generate a single URL for the user to log in to the target application without any redirects. The generated URL can be embedded in email or documents and would result in IDP Initiated SSO.

## Acknowledgements

- [Jack Stromberg's Site](https://jackstromberg.com/adfs-relay-state-generator/) (I stole the code in case his site ever goes offline. I did try to fancy it up a little bit with some CSS/)
- [BMC Docs](https://docs.bmc.com/docs/BMCHelixRemedyforce/201902/en/adfs-2-0-relay-state-868129786.html) (I stole the copy for the ReadMe above)
- [Really old Microsoft blog about RelayState](https://learn.microsoft.com/en-us/archive/blogs/askds/ad-fs-2-0-relaystate)

## Demo

[https://anthonycastaneda.github.io/RelayState_Generator](https://anthonycastaneda.github.io/RelayState_Generator)

## License

[MIT](https://choosealicense.com/licenses/mit/)
