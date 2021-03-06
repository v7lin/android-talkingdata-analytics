# android-talkingdata-analytics

[![Build Status](https://cloud.drone.io/api/badges/v7lin/android-talkingdata-analytics/status.svg)](https://cloud.drone.io/v7lin/android-talkingdata-analytics)
[![GitHub tag](https://img.shields.io/github/tag/v7lin/android-talkingdata-analytics.svg)](https://github.com/v7lin/android-talkingdata-analytics/releases)
[![API](https://img.shields.io/badge/API-14%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=14)

### snapshot

````
ext {
    latestVersion = '4.0.21-SNAPSHOT'
}

allprojects {
    repositories {
        ...
        maven {
            url 'https://oss.jfrog.org/artifactory/oss-snapshot-local'
        }
        ...
    }
}
````

### release

````
ext {
    latestVersion = '4.0.21'
}

allprojects {
    repositories {
        ...
        jcenter()
        ...
    }
}
````

### usage

android
````
...
android {
    ...
    defaultConfig{
        ...
        manifestPlaceholders = [TENCENT_APP_ID: "${appId}"]
        ...
    }
    ...
}
...
dependencies {
    ...
    implementation "io.github.v7lin:talkingdata-analytics-android:${latestVersion}"
    ...
}
...
````
