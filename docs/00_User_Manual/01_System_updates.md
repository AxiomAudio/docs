## Volumio OTA Updater

Volumio features an OTA (Over The Air) updater, meant to allow seamless and reliable way to update to new system versions. This is what the Volumio OTA updater allows:

* Volumio uses a cloud-based build mechanism for its images, which includes the updater control backbone
* 1:1 verified updates of new versions, this ensures that new updates are deployed exactly as they are built
* Differential download: instead of downloading the full firmware, Volumio will download just the differences beetween the current system and the new one. This allows to save up to 90% of download size, resulting also in faster downloads
* User-data preservation: updating to a new version will keep user data (such as playlists, music files, settings) untouched
* Ability to reset to factory settings: doing so will revert the system to the first version it was booted to. This will cancel both user data and newer system versions
* Ability to wipe user-data: doing so will reset all settings to factory defaults, while keeping the last firmware version installed.

### How to use the OTA updater

* Verify that your Volumio device is connected to the Internet
* Click on the cog-wheel in the top right part of the UI
* Select system
* Click on "Check Updates"
* If an update is available, you'll be presented with the new features.
* Click on "Update Now"
* System update will start, and depending on the update size it might take up to 20 minutes
* Once Update has finished, you'll be asked to reboot. Do it
* The system will now restart, and new version will be applied

### Use the system updater to test Beta-Releases

* Volumio can be updated to Beta Releases via OTA Updater. Beta-releases are test builds of the system with undisclosed functionalities
* Beta releases are meant to test new functionalities before deploying an update to the entire Volumio userbase
* Beta releases might not work, or present bugs still to be solved. They are therefore meant for expert users willing to take the risk to loose all their data
* To receive beta-releases, the system has to be put in "TEST MODE". To do so, navigate to http://volumio.local/dev or http://yourvolumioip/dev
* Once in the /dev page, click on  "TRUE" on "TEST MODE" Section. Your device is now in TEST MODE, and will receive test updates from now on
* Follow the above instructions to update your system normally, the only difference is that you'll see the test releases in spite of ordinary releases

### Disable TEST MODE

* To disable test mode, navigate to /dev page and click "FALSE" on "TEST MODE" section.
* You will now receive only ordinary releases
* In case you want to revert to old stable release, do a factory reset and then update to latest stable version (this will erase all your data)

### Considerations over OTA Updater

* If you're an advanced user and do usually manual settings to the system (e.g. manual changes of config files via SSH, update volumio backend via GIT etc) , we strongly suggest not to USE the OTA updater, since your manual changes will impact the consistency of the updates
