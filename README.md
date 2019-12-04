# JCenter

## How to use: 

1 - Create a new Maven/Package on Bintray

2 - Add To the **top-level build.gradle** :

```
dependencies {
    classpath 'com.android.tools.build:gradle:1.2.3'
    classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.2'
    classpath 'com.github.dcendents:android-maven-plugin:1.2'
}
```

3 - Add to the library's module **build.gradle** (below apply plugin):

```
ext {
    bintrayRepo = 'maven'
    bintrayName = 'example-lib'

    // Maven metadata
    publishedGroupId = 'eu.giovannidefrancesco.examplelib'
    libraryName = 'Example-Lib'
    artifact = 'examplelib'

    libraryDescription = 'Desc'
    libraryVersion = '0.1'

    developerId = 'devId'
    developerName = 'dev name'
    developerEmail = 'dev email'
}
```

4 - at the bottom of the same file, add:

```
apply from: 'https://raw.githubusercontent.com/githubUsername/JCenter/master/installv1.gradle'
apply from: 'https://raw.githubusercontent.com/githubUsername/JCenter/master/bintrayv1.gradle'
```

5 - **local.properties**:

```
bintray.user=devBintrayUsername
bintray.apikey=(BINTRAY_API_KEY)
```
