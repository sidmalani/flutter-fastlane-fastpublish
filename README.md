# flutter-fastlane-fastpublish
Starter flutter template project for developers to speed up publishing of flutter projects to playstore and appstore.

## Prerequisites

- Get Google Play and Apple Developer accounts.
- Get key generated from playstore as a json file.

## Setup github secrets as follows

- ANDROID_KEYSTORE_FILE - base 64 value of the contents of your keystore.jks
  - ``` base64 -i keystore.jks > keystore.jks.b64 ```
- KEYSTORE_STORE_PASSWORD - keystore file password
- KEYSTORE_KEY_ALIAS - key alias
- KEYSTORE_KEY_PASSWORD - key password
- PLAY_CONFIG_JSON - base 64 value of the contents of playstore key json file
  - ``` base64 -i play_config.json > play_config.json.b64 ```


Please note the first aab file may have to be uploaded manually according to some blog posts. So just create a release in Playstore in internal testing and upload the ".aab" file. Mark it versionName 0.0.1 and versionNumber 1.

To release newer versions simply update the version in pubspec.yaml file. The format is <versionname>+<versionnumber> so increment both and publish.

The current setup releases beta track to "Internal Testing" in Playstore.
