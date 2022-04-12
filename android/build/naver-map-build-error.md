
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

## 안된 이유
공식문서에 따르면

- android.useAndroidX=true
   - Android 플러그인은 지원 라이브러리 대신 적절한 AndroidX 라이브러리를 사용합니다.
- android.enableJetifier=true
   - Android 플러그인은 바이너리를 다시 작성해 기존 타사 라이브러리를 자동으로 이전하여 AndroidX를 사용합니다.

즉 지도 SDK 가 android support 라이브러리를 지원하고 있었기에
위 두 설정을 true로 해줌으로서 android support 라이브러리를 적절한 androidx 라이브러리를 사용하도록 한다.
androidx로 migration 한 것!

androidx support를 true 로 설정해주어도 모든 외부 라이브러리를 처리하지 못할 수 있다.
이에 관한 내용은 [요기서](https://developer.android.com/jetpack/androidx/migrate?hl=ko#mappings) 확인할 수 있다.

아마도 이 때문인 것 같음 ㅎ
