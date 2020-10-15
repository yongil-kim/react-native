## React, React-Native란? 

> **React**는 **Facebook**의 **오픈 소스 라이브러리**로 웹 프론트 개발을 편리하게 하기 위해 만들어졌습니다.<br>
> 그리고 **React Native**는 리액트의 접근 방법을 모바일로 확장한 오픈소스 프로젝트입니다! <br>
> 즉, React의 규칙을 이용하여 모바일 어플리케이션 개발을 할 수 있습니다.<br>
<br>

## 왜? React-Native를 사용하는가?

> 일반적으로 '**앱**' 개발하기 위해서는 각 플랫폼에 맞는 언어로 개발을 해야합니다. 

~~~bash
Android : java, Kotlin
iOS     : Objective-C, Swift
~~~

> 하지만 빠르게 앱을 만들어 시장 반응을 보려 하는 스타트업과 같은 곳에서는 두 가지를 동시에 개발하기에는 인력과 시간 소모가 큽니다. <br>
> 그래서 동시에 개발할 수 있는 **하이브리드** 앱이 나오게 되었는데 (대표적인 예로: ionic)<br>
> 하이브리드는 웹뷰를 네이티브에 씌우는 형태이기에 속도가 느리고 큰 규모의 프로젝트에는 적합하지 않습니다.<br>

### 그래서 React-Native가 나오게 되었습니다.

![bridge](https://github.com/yongil-kim/react-native/blob/main/resources/react-native-flow.png)

> React Native는 하이브리드 앱, 즉 아이오닉과 같은 웹뷰에 포팅된 형태의 어플리케이션이 아닙니다.
> **javascript**로 코딩한 **React Component**는 **React Native** 플랫폼을 거쳐 Android iOS Native 코드로 각각 변환됩니다.
> 즉, javascript 언어만으로도 앱 제작이 가능합니다.
<br>

## React-Native 장점

**1️⃣ 플랫폼 별 언어를 몰라도 Javascript만 알고 있어도 앱을 만들 수 있다.**

> 현재 RN이 점점 발전하여 왠만하게 쓰이는 기능들은 다 third-party 모듈이나 EXPO에서 제공을 해주고 있습니다. 

2️⃣ **개발 속도가 빠르다.**

> 생산성이 높은 편이며, 개발하면서 바로 결과를 확인 할 수 있게 Live Reloading을 제공해줍니다.
> Android, iOS는 코드를 변경할 때마다 빌드를 새로 하여 앱을 재기동 시키는 React-Native는 그러지 않아도 됩니다.

**3️⃣ 속도가 빠르다. (상대적)**

> 하이브리드 앱 보다는 속도가 월등이 빠르다. 

**4️⃣ 레퍼런스가 많다.**

> 높은 퍼포먼스와 생산성으로 인해 개발자들의 질의응답이 매우 활발한 편입니다.



## React-Native 단점

**1️⃣ React Native가 제공하는 기능은 한계가 있다.**

> 내가 필요한데 RN에는 없는 기능이라면 직접 Native로 제작해야 합니다. 그렇게 되면 결국 Android, iOS를 모두 할 줄 알아야 됩니다. 

**2️⃣ 성능 이슈**

> 크로스 플랫폼 앱의 특징처럼, 완벽하게 Native를 대체할 수는 없습니다.
> 비지니스 로직이 많이 복잡하거나 뷰 스택이 많이 쌓이게 된다면 속도는 느려집니다.



## React-Native 개발 환경 구성

**1️⃣ OS 개발 환경**

> OS는 **Windows, MacOS** 상관 없이 개발 환경을 구성이 가능합니다. 

- Windows : Android만 개발이 가능합니다.
- **MacOS**    : Android, iOS 모두 개발이 가능합니다.  ✅



**2️⃣ 리액트 네이티브 개발 방법**

1. **Expo CLI**

> **장점** : 앱을 개발할 때 자주 사용되는 네이티브 기능(위치 정보, 카메라 등)을 패키지로 묶어서 제공하기에 초기 구성이 편리합니다.
> **단점** : 사용하지 않은 네이티브 모듈로 인해 앱 파일 사이즈가 커지는 문제 Expo에서 제공하지 않은 네이티브 모듈을 추가할 때, 불편함 등이 있어 추천하지 않습니다.

2. **React Native CLI**  ✅

>**장점** : Third-party 모듈을 추가하기 편리하고, 제공하지 않는 네이티브 모듈이 있는 경우 Native 파일에 접근하여 직접 개발할 수 있다.
>**단점** : 초기 구성이 오래 걸리고, 배포가 불편하다.



3️⃣ **개발 환경 구축**

1. **Homebrew 설치**

> **설치**

~~~bash
sudo /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
~~~

> **버전 확인**

~~~bash
brew --version
============================================================================================================
Homebrew 2.5.3
Homebrew/homebrew-core (git revision 21fbd; last commit 2020-10-06)
Homebrew/homebrew-cask (git revision ff3c2d; last commit 2020-10-06)
~~~



2. **Nodejs 설치**

> **Nodejs 설치**

~~~bash
sudo brew install node
~~~

> **Nodejs 버전 확인**

~~~bash
node --version
============================================================================================================
v12.17.0
~~~

> **npm 버전 확인**  
>
> Nodejs를 설치하면, 기본적으로 Nodejs 패키지 매니저인 npm(Node Package Manager)도 같이 설치됩니다.

~~~bash
npm --version
============================================================================================================
6.14.4
~~~



3. **Watchman 설치**

> **설치**
>
> Watchman은 특정 폴더나 파일을 감시하다가 변화가 생기면, 특정 동작을 실행하도록 설정하는 역할을 합니다. 
> React-Native에서는 소스코드의 추가, 변경이 발생하면 다시 빌드하기 위해 Watchman을 사용하고 있습니다.

~~~bash
sudo brew install watchman
~~~

> **버전**

~~~bash
watchman --version
============================================================================================================
4.9.0
~~~



4. **React-Native CLI 설치**

> **설치**

~~~bash
sudo npm install -g react-native-cli
~~~

> **버전 확인**

~~~bash
react-native --version
============================================================================================================
react-native-cli: 2.0.1
react-native: n/a - not inside a React Native project directory
~~~



5. **XCode 설치**

> **설치**

~~~bash
App Store > XCode 검색 > 다운로드 & 설치
~~~

> **Command Line Tools 설정 확인**

~~~bash
XCode 실행 > 메뉴 > Preferences > Locations > Command Line Tools > XCode 12.0.1
~~~



6.  **CocoaPods 설치**

> **설치**
>
> React-Native로 iOS 앱을 개발하려면 꼭 필요하므로 아래에 명령어를 사용하여 Cocoapods를 설치합니다.

~~~bash
sudo gem install cocoapods
~~~

> **버전 확인**

~~~bash
pod --version
============================================================================================================
1.9.3
~~~



7. **jdk 설치**

> **설치**
>
> java 버전을 확인 했을 때 1.8 이상의 버전이 나온다면 설치하지 않으셔도 됩니다.

~~~bash
sudo brew tap AdoptOpenJDK/openjdk
sudo brew cask install adoptopenjdk8
~~~

> **버전 확인** 

~~~bash
java -version
============================================================================================================
openjdk version "1.8.0_265"
OpenJDK Runtime Environment (AdoptOpenJDK)(build 1.8.0_265-b01)
OpenJDK 64-Bit Server VM (AdoptOpenJDK)(build 25.265-b01, mixed mode)
~~~



8. **안드로이드 스튜디오 설치**

> **다운로드**

~~~bash
https://developer.android.com/studio
~~~

> **설치**

~~~bash
- Install Type : Custom 선택
- SDK Components Setup : Performance (Intel ® HAXM), Android Virtual Device 선택
- 기본 설치 진행
~~~

> **SDK Manager 설정**

~~~bash
- Android 9.0 (Pie) 또는 원하는 Version 설치
- Android SDK Build-Tools
- NDK
- Android Emulator
- Android SDK Platform-Tools
~~~

> **환경 변수 경로 설정**

~~~bash
vi ~/.bash_profile
export ANDROID_HOME=/Users/leby/Library/Android/sdk # Android SDK 경로 위치 
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools
============================================================================================================
source ~/.bash_profile
~~~

> **adb 확인**

~~~bash
adb --version
============================================================================================================
Android Debug Bridge version 1.0.41
Version 30.0.1-6435776
Installed as /Users/leby/Library/Android/sdk/platform-tools/adb
~~~





## React-Native 기본 프로젝트 생성 및 확인

> **현재 개발 버전 고정**
> React-Native는 버전에 따라, 잘 동작하던 앱이 동작을 안하거나, 빌드할 때 에러가 발생하는 등 여러 문제들을 일으킬 가능성이 높습니다. 
> 그러므로 React-Native로 앱을 개발할 때는 아래에 npm 명령어를 통해 버전을 고정시켜 사용하는 것을 권장합니다

~~~bash
npm config set save-exact=true
~~~

> **프로젝트 생성**
> React Native CLI를 이용하여 쉽게 프로젝트를 생성 할 수 있습니다.

~~~bash
react-native init SampleApp
~~~

> **iOS Simulator 실행**

~~~bash
cd SampleApp
# react-native run-ios
npm run ios
~~~

> **Android Emulator 실행**

~~~bash
cd SampleApp
# react-native run-android
npm run android
~~~



## React-Native 프로젝트 Native 라이브러리 포팅

> **Native 프로젝트 React-Native 프로젝트 라이브러리 비교 구성도**
> 라이브러리를 적용 시키는데 있어서는 Native 프로젝트와 React-Native 프로젝트는 동일하게 라이브러리를 적용 시키면 됩니다.
> 그렇다면 차이점은 Native 모듈을 구성하는데 있습니다.

![library](https://github.com/yongil-kim/react-native/blob/main/resources/library-flow.png)

>**Native** 프로젝트 같은 경우 Android, iOS **Native Project 각각의 카메라 모듈**을 구성하였는데, 
>**React-Native** 프로젝트는 **RNCamera** 모듈을 React-Native에서 호출하여 Android, iOS 공통 카메라 모듈을 사용합니다.

⚠️  하지만, 공통으로 카메라 모듈을 사용하다 보면 지원하지 않는 기능들이 있을 수 있습니다.
       예를 들어 실시간으로 카메라 프레임 가져오는 기능과 RN 모듈에서 제공하지 않는 기능들은 Native 별로 기능을 구현할 수 밖에 없습니다.



## React-Native Bridge 기능

> 브릿지 기능은 자바스크립트에서 android 또는 ios Native 엔진으로 메세지를 보내는 기능입니다.
> 즉, 연결해주는 브릿지 역할을 한다고 볼 수 있으며, 자바스크립트와 스마트폰의 커뮤니케이션을 월할하게 할 수 있도록 만들어졌습니다.
