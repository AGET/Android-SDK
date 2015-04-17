
## 0.4.3 (November 12, 2014):
 - Fixes https://github.com/Estimote/Android-SDK/issues/59: compatibilty with Android L

## 0.4.2 (June 24, 2014):
 - Fixes https://github.com/Estimote/Android-SDK/issues/55: it is safe to use library from remote process

## 0.4.1 (March 18, 2014)
 - *CAN BREAK BUILD*: MonitoringListener returns list of beacons the triggered enter region event (https://github.com/Estimote/Android-SDK/issues/18)
 - Better messaging when BeaconManager cannot start service to scan beacons (https://github.com/Estimote/Android-SDK/issues/25)
 - Fixed bug in SDK when other beacons are around (https://github.com/Estimote/Android-SDK/issues/27)

## 0.4 (February 17, 2014)
 - Introducing ability to change beacon's UUID, major, minor, broadcasting power, advertising interval (see BeaconConnection class).
 - Dropping Guava dependency.

## 0.3.1 (February 11, 2014)
 - Fixes bug when simulated beacons were not seen even when using Estimote's proximity UUID.

## 0.3 (February 11, 2014)
 - Background monitoring is more robust and using AlarmService to invoke scanning.
 - Default values for background monitoring were changed. Scanning is performed for 5 seconds and then service sleeps for 25 seconds. Those values can be changed with BeaconManager#setBackgroundScanPeriod.
 - Beacons reported in RangingListener#onBeaconsDiscovered are sorted by accuracy (estimated distance between device and beacon).
 - Bug fixes.

## 0.2 (January 7, 2014)
 - *IMPORTANT*: package changes BeaconService is now in `com.estimote.sdk.service service`. You need to update your `AndroidManifest.xml` service definition to `com.estimote.sdk.service.BeaconService`.
 - Support for monitoring regions in BeaconManager.
 - Region class: it is mandatory to provide region id in its constructor. This matches CLRegion/ESTBeaconRegion from iOS.
 - Beacon, Region classes now follow Java bean conventions (that is getXXX for accessing properties).
 - Debug logging is disabled by default. You can enable it via `com.estimote.sdk.utils.L#enableDebugLogging(boolean)`.

## 0.1 (December 9, 2013)
 - Initial version.