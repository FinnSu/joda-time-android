# Changelog

# 2.8.0

* [#47](https://github.com/dlew/joda-time-android/pull/47) Fixed compatibility w/ Android Gradle plugin 1.3
* [#51](https://github.com/dlew/joda-time-android/pull/51) Updated to joda-time 2.8
* [#52](https://github.com/dlew/joda-time-android/pull/52) Updated to tzdata 2015
* [#57](https://github.com/dlew/joda-time-android/pull/57) Added instructions for proguarding and using joda-convert

# 2.7.2

* Updated to tzdata 2015b

# 2.7.1

* Updated to tzdata 2015a
* Use joda-time's ZoneInfoCompiler (for bugfixes/consistency)

# 2.7.0

This release includes couple (possibly) breaking changes to previous versions of joda-time-android, depending on how
your project was configured.

#### Dependencies

Previously, joda-time-android included joda-time sources itself. Due to improvements made to the main project, it is
now possible for us to properly use the joda-time dependency. This means that:

1. If you are using Gradle, nothing should change, unless you were doing something weird.

2. If you're using Eclipse libraries, you will have to manually include joda-time.jar yourself now; make sure to
   get the no-tzdb artifact.

#### Initialization

Initially you initialized the library via `ResourceZoneInfoProvider.init()`. Later this was moved to
`JodaTimeAndroid.init()`. We're removing the other endpoint because it just makes this more difficult to
maintain; it should be simple to change from one to the other.

#### Other changes

* Updated to joda-time 2.7

# 2.6.0

* Updated to joda-time 2.6

# 2.5.1

* Modified how default DateTimeZone is updated by system (#20)
* Updated to tzdata 2014j

# 2.5.0

* Updated to joda-time 2.5
* Updated to tzdata 2014i

# 2.4.1

* Updated to tzdata 2014h

# 2.4.0

* Updated to joda-time 2.4

# 2.3.4

* `#10` Receive TIMEZONE_CHANGED broadcasts only when running, add JodaTimeAndroid.init
* Updated to tzdata 2014e

# 2.3.3

* `#4` Added library sample app
* `#9` Reset default DateTimeZone when TIMEZONE_CHANGED broadcast is received

## 2.3.2

* `#7` Added DateUtils.formatDuration()

## 2.3.1

* `#5` Add compatibility version of DateUtils
* `#6` Fixed lint error

## 2.3

* Initial port of joda-time to Android