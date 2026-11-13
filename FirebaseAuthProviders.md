# Providers
## Google
*Important: Allow Google Sign-in, add SHA-1 ```(./gradlew signingReport)``` in the console and re-download google-services.json.*
```
provider(
    AuthProvider.Google(
        scopes = listOf("email"),
        serverClientId = getString(R.string.default_web_client_id),
    )
)
```
## Email
```
provider(
    AuthProvider.Email(
        isDisplayNameRequired = true,
        isEmailLinkSignInEnabled = false,
        isEmailLinkForceSameDeviceEnabled = true,
        emailLinkActionCodeSettings = null,
        isNewAccountsAllowed = true,
        minimumPasswordLength = 6,
        passwordValidationRules = emptyList(),
    )
)
```
## Phone
*Important: add both SHA-1 and SHA-256 in the console. For testing without real SMS, add test phone numbers under Phone → “Phone numbers for testing”.*
```
provider(AuthProvider.Phone())
```
