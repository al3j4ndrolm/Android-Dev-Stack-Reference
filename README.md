## UI
### Fonts
- **[Google Downloadable Fonts API](https://developer.android.com/develop/ui/compose/text/fonts#use-downloadable-fonts)** : Use [Google Fonts](https://fonts.google.com/?preview.layout=grid) without adding the assets to the project
## Firebase
### [Google Services](https://github.com/google/play-services-plugins/blob/main/google-services-plugin/README.md)
 1. Add to the project level gradle : ```id("com.google.gms.google-services") version CHECK_VERSION apply false")```
 2. Add to the app level gradle : ```id("com.google.gms.google-services")```
### Authentication
- **[Firebase Pre-Built Sign-in UI](https://firebase.google.com/docs/auth/android/firebaseui)** : Provides a Sign-in button from multiple providers. Ex. "Sign in with Google"
   - To obtain SHA-1 : ```./gradlew signingReport```
   - [See repository documentation](https://github.com/firebase/FirebaseUI-Android/blob/master/auth/README.md#high-level-api-recommended)
  ### Providers
  ---
  **Google :**
  ```
  provider(AuthProvider
          .Google(
              scopes = listOf("email"),
              serverClientId = getString(R.string.default_web_client_id)
          )
  )
  ```
- **[Email & Password Auth](https://firebase.google.com/docs/auth/android/password-auth)** : How to implement email & password auth for an app
## Dependency Injection
 - **[Hilt](https://developer.android.com/training/dependency-injection/hilt-android#kts)** : To inject repositories, modules and viewmodels (and cache them)
   - **Needs : [KSP](https://kotlinlang.org/docs/ksp-quickstart.html)**
 - **[Hilt Compose](https://developer.android.com/training/dependency-injection/hilt-jetpack)** : To use **hiltViewModel()** in Jetpack Compose

