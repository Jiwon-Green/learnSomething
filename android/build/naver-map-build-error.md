
## 안되는 것
[네이버 지도 SDK](https://navermaps.github.io/android-map-sdk/guide-ko/1.html) 따라서 하다가 빌드부터 막힘. <br>
1. 프로젝트단 `build.gradle` 에 `maven {url 'https://naver.jfrog.io/artifactory/maven/'}` 추가 <br>
2. 앱단 `build.gradle`에 `implementation 'com.naver.maps:map-sdk:3.13.0'` 추가 <br>

<br>
빌드 돌리니 naver map-sdk:3.13.0 `Failed to resolve` 뜸 😡 <br>


## 해결
`settings.gradle` 에도 `maven {url 'https://naver.jfrog.io/artifactory/maven/'}` 추가하니까 됐다!

<br>


![image](https://user-images.githubusercontent.com/95398241/150718635-98af34ed-fdc5-4939-9269-c4ac7e48b6a6.png)

그리고 이 부분에서는 androidx 랑 충돌난다던데 `gradle.properties` 에 아래 두줄 추가하면 된다고 함 <br>

```
android.useAndroidX=true
android.enableJetifier=true
```
