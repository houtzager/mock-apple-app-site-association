# mock-apple-app-site-association
A Docker Compose project for easily mocking your apple-app-site-association.

In order to support features like Universal links or Handoff, Apple requires you to upload an apple-app-site-association file to your website. This library allows you to mock this locally first so you can design and test the apple-app-site-association file yourself, without depending on a website.


## Requirements

* Docker Compose
* Basic Docker knowledge

## Usage

1. Ensure you have Docker Compose installed and running on your computer.
2. Configure the apple-app-site-association file as desired.
3. Run `docker-compose up` from the root of this project.
    * You can also put a `-d` tag at the end to run in detached mode.
4. Specify the url that shows up in your log in your app's Entitlements. _Note: the url changes each time you restart the compose configuration._
5. Delete the app from your simulator or device.
6. Reinstall the app.
7. Use the url with configured format in the `app-site-association-domain` to test opening the app with a universal link. 

## References

* Documentation about supporting universal links for your app: https://developer.apple.com/library/archive/documentation/General/Conceptual/AppSearch/UniversalLinks.html
