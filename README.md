# flutter-fastlane-fastpublish
Starter flutter template project for developers to speed up publishing of flutter projects to playstore and appstore.

## Prerequisites

- Get a playstore and appstore accounts.
- Get key generated from playstore as a json file.

## Setup github secrets as follows

- ANDROID_KEYSTORE_FILE - base 64 value of the contents of your keystore.jks
- KEYSTORE_STORE_PASSWORD - keystore file password
- KEYSTORE_KEY_ALIAS - key alias
- KEYSTORE_KEY_PASSWORD - key password
- PLAY_CONFIG_JSON - base 64 value of the contents of playstore key json file
