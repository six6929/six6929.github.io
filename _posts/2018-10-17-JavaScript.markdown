---
layout: post
title:  "JavaScript"
date:   2018-10-17 22:09:11 +0000
categories: Web
excerpt : HTML과 CSS는 정적인 언어인 반면, <b>JavaScript는 HTML과 CSS로 만들어진 웹페이지를 동적으로 변경해주는 언어입니다. 자바스크립트는 원래는 잘 사용되지 않는 스트립트 언어였습니다. 하지만 구글에서 지도 서비스를 HTML/CSS와 JavaScript만을 이용해 플래쉬와 같은 효과를 구현하면서 자바스크립트 열풍이 불기 시작했다고합니다.
image: gitProfile.jpg
---
<JavaScript 정리>
<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript 정의</h3>
<br>
HTML과 CSS는 정적인 언어인 반면, <b>JavaScript는 HTML과 CSS로 만들어진 웹페이지를 동적으로 변경해주는 언어입니다.</b> 자바스크립트는 원래는 잘 사용되지 않는 스트립트 언어였습니다. 하지만 구글에서 지도 서비스를 HTML/CSS와 JavaScript만을 이용해 플래쉬와 같은 효과를 구현하면서 자바스크립트 열풍이 불기 시작했다고합니다.
<br>
<iframe src="https://six6929.github.io/DIGB313/Homework7/Homework7.html" style=" width:100%; height:300px;"></iframe>
<br>
위 구글 지도서비스는 제가 HTML/CSS와 JavaScript로 구현해 본 예제입니다.<br>
이제부터 JavaScript를 자세하게 배워 저렇게 만들 수 있도록 알아보도록 하겠습니다.<br>
<br>
<hr>

<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript 변수선언</h3>
<br>
자바스크립트에서 변수는 값과 연관된 이름으로서, 변수를 이용하면 데이터를 저장하고 조작할 수 있습니다.
<br>
변수는 var 키워드로 선언합니다.
<br>
동일한 var 키워드를 이용해서 여러 개의 변수를 선언할 수 있으며, 선언함과 동시에 초기화 할 수도 있습니다.
<br>
<img src="{{ site.baseurl }}/images/JavascriptEx_1.png" style="width:100%" alt="">
<br>
자바스크립트는 Java나 C언어와 달리 명시적인 타입이 필요하지 않습니다. 자바스크립트 변수는 어떤 자료형의 값도 var 안에 담을 수 있으며, 한 변수를 다른 타입의 값으로 초기화 또는 할당할 수 있습니다.
<br>
<hr>
<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript 전역변수와 지역변수</h3><br>
<ul>
  <li> 전역변수는 코드 내에서 어디서든 변수에 접근할 수 있는 변수를 의미합니다.</li>
  <li> 지역변수는 함수 내에서 변수를 정의하고 접근할 수 있는 변수를 의미합니다.</li>
  <li> 함수 매개변수도 지역 변수로 간주하며 해당 함수의 본문 내에서 접근할 수 있습니다.</li>
  <li> 지역 변수와 전역 변수의 이름이 같을 경우 지역 변수가 우선순위가 높습니다. </li>
</ul>
<br>
전역 변수와 지역 변수의 예를 보여드리겠습니다.
<pre style="border:2px dotted #A8A8A8; white-space:pre-line; word-break:break-all;">
                  var name = "global";    //전역 변수를 선언
                  function checkscope() {
                      var name = "local"; //지역 변수를 선언
                      console.log(name);  //전역 변수가 아닌 지역 변수를
                  }
                  checkscope();
</pre>
<hr>
var 키워드 없이 변수를 선언하면 자동으로 전역 변수가 됩니다.

<pre style="border:2px dotted #A8A8A8; white-space:pre-line; word-break:break-all;">
                  var name = "global"     // 전역 변수를 선언
                  function checkscope() {
                      name = "local";     //전역 변수를 변경
                      name2 = "local";    //암묵적으로 새 전역 변수가 선언됨
                  }
                  checkscope();
                  console.log(name);      //output: "local"
                  console.log(name2);     //output: "local"
</pre>
<br>

<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript 출력</h3>
<br>
자바스크립트는 여러 방법을 통해 결과물을 HTML 페이지에 출력할 수 있습니다.<br>
자바스크립트에서 사용할 수 있는 출력 방법은 다음과 같습니다.
<ol>
  <li>window.alert() Method</li>
  <li>HTML DOM 요소를 이용한 innerHTML property</li>
  <li>document.write() Method</li>
  <li>console.log() Method</li>
</ol>
<hr>
<h3><b>document.write() Method</b></h3>
document.write() 메서드는 웹 페이지가 로딩될 때 실행되면, 웹 페이지에 가장 먼저 데이터를 출력합니다. 따라서 document.write() 메서드는 대부분 테스트나 디버깅을 위해 사용됩니다.
<br>
<br>
<img src="{{site.baseurl}}/images/jsWrite.png" style="width:100%" alt="">
하지만 웹 페이지의 모든 내용이 로딩된 후에 document.write() 메서드가 실행되면, 웹 페이지 내에 먼저 로딩된 모든 데이터를 지우고 자신의 데이터를 출력하게 됩니다.
<br>
<br>
<img src="{{site.baseurl}}/images/jsWrite2.png" style="width:100%" alt="">

<hr>
<h3><b>document.alert() Method</b></h3>
자바스크립트에서 가장 간단하게 데이터를 출력할 수 있는 방법은 window.alert() 메소드를 이용하는 것입니다. window.alert() 메소드는 브라우저와는 별도의 대화 상자를 띄워 사용자에게 데이터를 전달해줍니다.
<br>
<br>
<img src="{{site.baseurl}}/images/jsWrite3.png" style="width:100%" alt="">
<br>
<hr>
<h3><b>HTML DOM 요소를 이용한 innerHTML property</b></h3>
<br>
우선 document 객체의 getElementByID()나 getElementByTagName() 등의 메소드를 사용하여 HTML 요소를 선택합니다. 그리고서 innerHTML property를 이용하면 HTML 요소의 내용(content)이나 속성(attribute) 값 등을 손쉽게 변경할 수 있습니다.
<br>
<br>
<img src="{{site.baseurl}}/images/jsWrite4.png" style="width:100%" alt="">

<hr>
<h3><b>console.log() Method</b></h3>
console.log() 메서드는 웹 브라우저의 콘솔을 통해 데이터를 출력해줍니다.
<br>
대부분의 주요 웹 브라우저에서는 F12를 누른 후, 메뉴에서 콘솔을 클릭하면 콘솔화면을 사용할 수 있습니다. 이러한 콘솔 화면을 통한 데이터의 출력은 좀 더 자세한 사항까지 출력되므로, 디버깅하는데 많은 도움을 줍니다.
<br>
<br>
<img src="{{site.baseurl}}/images/jsWrite5.png" style="width:100%" alt="">
<hr>

<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript 연산자</h3>
자바스크립트에는 증감연산자(++, --), 산술연산자(+, -, *, /, %), 대입연산자(=, +=, -=, *=, /=, %=), 비교연산자(>, <, >=, <=, ==, !=, ===, !==)있습니다. 여기서 Java, C언어와 다르게 ===, !==가 있는 것을 볼 수 있습니다.
<br>

&gt;==, !=&lt; , &gt;===, !==&lt;의 차이점을 예를 들어서 보여드리겠습니다.
<br>
<img src="{{site.baseurl}}/images/jsCalc.png" style="width:100%" alt="">
