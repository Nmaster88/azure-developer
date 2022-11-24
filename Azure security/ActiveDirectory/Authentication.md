Information about AAD Authentication can be found in the link
https://learn.microsoft.com/en-us/azure/active-directory/authentication/

# Authentication methods

## What authentication and verification methods are available in Azure Active Directory?

Microsoft recommends passwordless authentication methods such as Windows Hello, FIDO2 security keys, and the Microsoft Authenticator app because they provide the most secure sign-in experience.

![image](https://user-images.githubusercontent.com/12272451/203771309-24d401ab-aa4a-4668-9421-492ee3eb8132.png)


## Authentication method strength and security

|Authentication method|Security|Usability|Availability|
|-|-|-|-|
|Windows Hello for Business|High|High|High|
|Microsoft Authenticator app|High|High|High|
|FIDO2 security key|High|High|High|
|Certificate-based authentication (preview)|High|High|High|
|OATH hardware tokens (preview)|Medium|Medium|High|
|OATH software tokens|Medium|Medium|High|
|SMS|Medium|High|Medium|
|Voice|Medium|Medium|Medium|
|Password	|High|High|High|

## How each authentication method works

Some authentication methods can be used as the primary factor when you sign in to an application or device, such as using a FIDO2 security key or a password. Other authentication methods are only available as a secondary factor when you use Azure AD Multi-Factor Authentication or SSPR.

|Method|Primary authentication|Secondary authentication|
|-|-|-|
|Windows Hello for Business|Yes|MFA*|
|Microsoft Authenticator app|Yes|MFA and SSPR|
|FIDO2 security key|Yes|MFA|
|Certificate-based authentication (preview)|Yes|No|
|OATH hardware tokens (preview)|No|MFA and SSPR|
|OATH software tokens|No|MFA and SSPR|
|SMS|Yes|MFA and SSPR|
|Voice call|No|MFA and SSPR|
|Password|No||

# Authentication strenghts

## Conditional Access authentication strenght

Authentication strength is a Conditional Access control that allows administrators to specify which combination of authentication methods can be used to access a resource. For example, they can make only phishing-resistant authentication methods available to access a sensitive resource. But to access a nonsensitive resource, they can allow less secure multifactor authentication (MFA) combinations, such as password + SMS.

## Built-in authentication strengths

The following table lists the combinations of authentication methods for each built-in authentication strength. Depending on which methods are available in the authentication methods policy and registered for users, they can use any one of the combinations to sign-in.

- MFA strength - the same set of combinations that could be used to satisfy the Require multifactor authentication setting.
- Passwordless MFA strength - includes authentication methods that satisfy MFA but don't require a password.
- Phishing-resistant MFA strength - includes methods that require an interaction between the authentication method and the sign-in surface.

|Authentication method combination|MFA strength|Passwordless MFA strength|Phishing-resistant MFA strength|
|-|-|-|-|
|FIDO2 security key|✅|✅|✅|
|Windows Hello for Business|✅|✅|✅|
|Certificate-based authentication (Multi-Factor)|✅|✅|✅|
|Microsoft Authenticator (Phone Sign-in)|✅|✅||
|Temporary Access Pass (One-time use AND Multi-use)|✅|||
|Password + something you have1|✅|||
|Federated single-factor + something you have1|✅|||
|Federated Multi-Factor|✅|||
|Certificate-based authentication (single-factor)||||
|SMS sign-in||||
|Password||||
|Federated single-factor||||

## Azure AD Multi-Factor Authentication

The following additional forms of verification can be used with Azure AD Multi-Factor Authentication:

- Microsoft Authenticator app
- Windows Hello for Business
- FIDO2 security key
- OATH hardware token (preview)
- OATH software token
- SMS
- Voice call

![image](https://user-images.githubusercontent.com/12272451/203775204-70e1803d-da2a-4fa8-bd55-83423315b2f7.png)


