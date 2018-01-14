# ReactNativeSDK

### Automatic installation
`$ npm install react-native-ziggeo-library --save`

### Manual installation
#### Android
1. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-ziggeo-library'
  	project(':react-native-ziggeo-library').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-ziggeo-library/android')
  	```

2. Open up `android/build.gradle`
	- Insert the following line inside the `allprojects/repositories` block:
	```
	maven { url 'https://jitpack.io' }
	```
  	
3. Open up `android/app/build.gradle`
	- Update `compileSdkVersion`, `buildToolsVersion`, `targetSdkVersion` and all libs from `com.android.support` package to latest versions.
	- Insert the following line inside the `dependencies` block:
	```
	compile project(':react-native-ziggeo-library')
	```

4. Open up `android/app/AndroidManifest.xml` 
	- Insert the following line inside the `manifest` block:
	```
	xmlns:tools="http://schemas.android.com/tools"
	```
	- Insert the following line inside the `application` block:
	```
	tools:replace="android:name"
	```

5. Open up `android/app/src/main/java/[...]/MainActivity.java`
  	- Change `extends ReactActivity` to `extends ReactFragmentActivity`
  	- Add `import com.ziggeo.ZiggeoPackage;` to the imports at the top of the file

6. Open up `android/app/src/main/java/[...]/MainApplication.java`
  	- Add `new ZiggeoPackage()` to the list returned by the `getPackages()` method

## Usage
```javascript
import Ziggeo from 'react-native-ziggeo-library';
```
