# flutter-fastlane-fastpublish
Starter flutter template project for developers to speed up publishing of flutter projects to playstore and appstore.

## Refer to this blog for some setup pointers

https://medium.com/scalereal/automate-publishing-app-to-the-google-play-store-with-github-actions-fastlane-ac9104712486

## Prerequisites

- Get Google Play and Apple Developer accounts.
- Get key generated from playstore as a json file. 
- Keystore setup.


# Android Playstore

## First time

- Ensure you create a keystore file and key.
- Sign the aab file with the key.
- Upload manually to playstore, create a release 0.0.1, version Number 1 in the internal testing track.
- Once this is done future can be run via Github pipeline.


## Setup github secrets as follows

- ANDROID_KEYSTORE_FILE - base 64 value of the contents of your keystore.jks
  - ``` base64 -i keystore.jks > keystore.jks.b64 ```
- KEYSTORE_STORE_PASSWORD - keystore file password
- KEYSTORE_KEY_ALIAS - key alias
- KEYSTORE_KEY_PASSWORD - key password
- PLAY_CONFIG_JSON - base 64 value of the contents of playstore key json file
  - ``` base64 -i play_config.json > play_config.json.b64 ```

## Future releases

To release newer versions simply update the version in pubspec.yaml file. The format is <versionname>+<versionnumber> so increment both and publish.
  

## Promote to Production

The current setup releases beta track to "Internal Testing" in Playstore. From there you can simply release to production.
  
# Apple Appstore

TBC...

Please reportn any issues so we can keep this up to date.
