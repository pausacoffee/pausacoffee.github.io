---
layout: post
title: 맥에 flutter를 설치해보자!
subtitle: How to Install Flutter for Macwith Visutal Studio Code
categories: Flutter
tags: [Flutter, VSCode, Install, Mac]
---

<H1>설치하기</H1>
<p>
  Flutter는 Google에서 제공하는 오픈소스 프레임워크입니다. Dart언어를 사용하며, 크로스플랫폼 개발 툴입니다.
</p>
<p>
  <b>Mac 환경에서 Flutter를 설치해봅시다.</b>
</p>
<br/>
<br/>
<H3>Flutter 설치</H3>
<p>
  1. 아래의 url로 이동하여 SDK를 다운로드해주세요.
</p>
<pre>
https://docs.flutter.dev/get-started/install/macos
</pre>
<br/><p>2. Get the Flutter SDK 아래에 있는 링크로 파일을 다운로드 해주세요</p>
<p> > 2022-05-02 기준 'flutter_macos_2.10.5-stable.zip'</p>
<br/><p>3. 원하는 곳에 unzip 합니다.</p>
<p> > 필자는 Documents/Work/SDK 하위에 unzip</p>
<p> > Documents/Work/SDK/flutter 폴더가 생성됨.</p>
<br/><p>4. sublime Text 앱을 설치합니다.</p>
<pre>https://www.sublimetext.com/
</pre>
<p> > 다운로드 파일을 압축해제 후, 앱을 Applications로 옮겨 줍니다.</p>
<br/><p>5. 아래의 url로 이동하여 환경변수를 생성합니다.</p>
<pre>
https://docs.flutter.dev/get-started/install/macos#update-your-path
</pre>
<p> > sublime text 에 아래 내용을 붙여넣습니다(본인이 어디에 flutter를 unzip 했는지 쓰세요!)</p>
<p> > export PATH="$PATH:<b>Documents/Work/SDK/flutter</b>/bin"</p>
<p> > 저장 경로는 '내컴퓨터 이름'($HOME), 저장 이름은 '.zshrc'로 합니다.</p>
<br/><p>6. 터미널을 열어 <b>source $HOME/.zshrc</b> 그리고 <b>echo $PATH</b>를 차례로 입력합니다.</p>
<p> > 터미널은 command + space 로 Spotlight를 열어 terminal 을 입력하면 켜집니다.</p>
<br/><b>여기까지 따라 오셨으면 터미널에서 'flutter' 커맨드가 가능합니다!</b><br/><br/>
<br/><p>7. 터미널에 'flutter doctor'를 입력하여 정상 설치를 확인합니다. </p>  
<p>자세히 읽어 보시면 XCode, Andriod Studio, VS Code에 빨간 불이 들어오셨을 것입니다.</p>

<br/><br/>
<H3>VSCode 설치</H3>
<p>
  1. 아래의 url로 이동하여 VS Code를 설치해주세요.
</p>
<pre>
https://code.visualstudio.com/
</pre>
<p> > 다운로드 파일을 압축해제 후, 앱을 Applications로 옮겨 줍니다.</p>
<br/><p>2. 왼쪽 사이드 바에서 '확장'으로 이동합니다.</p>
<br/><p>3. 'dart'와 'flutter'를 각각 검색하여 인스톨해줍니다.</p>
<br/><p>4. 터미널에 'flutter doctor'를 입력하여 정상 설치를 확인합니다. </p>  
<br/><br/>
<H3>Android Studio 설치</H3>
<p>
  1. 아래의 url로 이동하여 Android Studio를 설치해주세요.
</p>
<pre>
https://developer.android.com/studio?gclid=Cj0KCQjw37iTBhCWARIsACBt1IzKAjxURMwZHTlV2SqtTzgC_F0dMNIcgquJ9CPFEXNIcJu9nHOM_lsaAlpVEALw_wcB&gclsrc=aw.ds#downloads
</pre>
<p> > 내 컴퓨터에 맞는 버전을 확인하고 다운로드 받으세요!</p>
<p> > 아이콘을 Applications로 이동하면 자동으로 다운됩니다.</p
<br/><p>2. 설치가 완료되고, 안드로이드 스튜디오가 실행되면 more Actions에 SDK Manager로 이동합니다. </p>  
<p> > 혹은 Tools - SDK Manager로 이동하면 됩니다.</p>
<br/><p>3. SDK Tools 탭으로 이동하여 'SDK Command-line Tools'를 체크 후 설치 합니다. </p>  
<p> > 본인은 필요에 의해 CMake, NDK 또한 설치함.</p>
<br/><p>4. 터미널에 'flutter doctor'를 입력하여 정상 설치를 확인합니다. </p>
<p> > 라이센스때문에 빨간불이 들어올 겁니다. 아래의 커맨드를 터미널에 입력하세요(혹은 터미널에 안내되는 커맨드를 실행하시면 됩니다.)</p>
<pre>
flutter doctor --android-licenses
</pre>
  
<br/><br/>
<H3>XCode 설치</H3>
<p>
  1. 앱스토어로 이동하여 'XCode'를 설치합니다. 혹은 아래의 url로 이동하여 자신이 개발해야 하는 swift버전에 맞는 XCode를 설치합니다.
</p>
<pre>
developer.apple.com/download/more/
</pre>
<p> > 안드로이드처럼 상위 swift 버전이 하위 swift 버전에 대한 대응을 못함.</p>
<p> > 여러버전의 XCode를 설치하여 swap하며 사용할수 있습니다.</p>
<br/><p>2. M1 사용자의 경우 아래 url로 이동하여 Rosetta2를 설치합니다. </p>
<pre>
https://github.com/flutter/flutter/wiki/Developing-with-Flutter-on-Apple-Silicon
</pre>
<br/><p>3. 터미널에 'flutter doctor'를 입력하여 정상 설치를 확인합니다. </p>
<p> > cocoapods not installed 가 뜨면 아래 url로 이동하여 설치합니다.</p>
<pre>
https://guides.cocoapods.org/using/getting-started.html
</pre>
<p> > XCode에서 안드로이드의 gradle과 같은 역할을 합니다.(의존성 관리 매니저)</p>

<br/><br/>
<H3>Chrome 설치</H3>
<p>
  Flutter는 크롬 브라우저 기반으로 웹을 빌드합니다.
</p>

