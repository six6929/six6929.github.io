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
<br>
자바스크립트에는 증감연산자(++, --), 산술연산자(+, -, *, /, %), 대입연산자(=, +=, -=, *=, /=, %=), 비교연산자(>, <, >=, <=, ==, !=, ===, !==)있습니다. 여기서 Java, C언어와 다르게 ===, !==가 있는 것을 볼 수 있습니다.
<br>

<==, !=> , <===, !==>의 차이점을 예를 들어서 보여드리겠습니다.
<br>
<img src="{{site.baseurl}}/images/jsCalc.png" style="width:100%" alt="">
<br>
그림에서 볼 수 있듯이 <==, !=> 값만 일치하면 되지만, <===, !==>는 값과 타입까지 동일해야 함을 알 수 있습니다.

<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript 객체</h3>
<br>
<b>객체(object)</b>란 실생활에서 우리가 인식할 수 있는 사물로 이해할 수 있습니다. <br>
<b>프로퍼티(property)</b>란 객체의 일부로 이름과 값 사이 연결을 의미라고 정의합니다. <br>
<b>메소드(Method)</b>란 객체가 가지고 있는 동작을 의미합니다.
<hr>
객체(object)
<br>
- TV <br>
<img src="{{site.baseurl}}/images/tv.jpg" style="width:30%" alt="">
<br>
<br>
프로퍼티(property)
<br>
tv.width = 1500; //속성 만들고, 값 설정 <br>
tv.height = 700; <br>
tv.color = "black"; <br>
tv.weight = "20kg";
<br>
<br>
메서드(Method)
<br>
tv.on();<br>
tv.off();

<hr>
<h3> 자바스크립트 객체 </h3>
자바스크립트의 기본 타입은 객체입니다.<br>
객체란 이름과 값으로 구성된 프로퍼티의 정렬되지 않은 집합입니다.<br>
프로퍼티의 값으로 함수가 올 수도 있는데, 이러한 프로퍼티를 메소드(method)라고 합니다.
<br>
<br>
객체 선언 및 사용<br>
<img src="{{site.baseurl}}/images/jsObject1.png" style="width:100%" alt="">
<br>
객체 프로퍼티 적용<br>
<img src="{{site.baseurl}}/images/jsObject2.png" style="width:100%" alt="">
<br>
객체 메소드 호출<br>
<img src="{{site.baseurl}}/images/jsObject3.png" style="width:100%" alt="">
<br>
자바스크립트에서는 숫자, 문자열, boolean, undefined 타입을 제외한 모든 것이 객체입니다. <br>
하지만 숫자, 문자열, boolean과 같은 원시 타입은 값이 정해진 객체로 취급되어, 객체로서의 특징도 함께 가지게 됩니다.
<br>
<hr>
객체 사용
<img src="{{site.baseurl}}/images/jsObject4.png" style="width:100%" alt="">
<br>
<p style="border:1px solid darkgray; font-size:80%"><i>주의 </i> : 메소드를 참조할 때는 괄호를() 붙이지 않으면, 메소드가 아닌 프로퍼티 자체를 참조하게 됩니다.</p>
<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript 이벤트</h3>
<br>
이벤트(event)란 웹 브라우저가 알려주는 HTML 요소에 대한 사건의 발생을 의미합니다.
<br>
웹 페이지에 사용된 자바스크립트는 이렇게 발생한 이벤트에 반응하여 특정 동작을 수행할 수 있습니다. 따라서 클라이언트 측 자바스크립트를 비동기식 이벤트 중심의 프로그래밍 모델이라고 합니다.
<hr>
<h3> 마우스 관련 이벤트 </h3>
<img src="{{site.baseurl}}/images/mouseEvent.png" style="width:100%" alt="">
위의 그림은 id가 imgbtn이라는 요소에 마우스를 올렸을때는  btn2_yellow이미지를 마우스가 벗어났을 때는 btn2_gray이미지를 나타낼 수 있게 마우스에다가 이벤트 효과를 주었음을 보여주고 있습니다.
<br>
실습한 내용을 가지고 이벤트에 대해서 더 알아보도록 하겠습니다.
<hr>
<h3> form 관련 이벤트 </h3>
<iframe src="https://six6929.github.io/BIT_Web/JavaScript/36_js_%EC%9D%B4%EB%B2%A4%ED%8A%B8_form.html" style="width:100%; height:400px"></iframe>
<br>
<img src="{{site.baseurl}}/images/formEvent1.png" style="width:100%" alt="">
<br>
확인 버튼을 눌렀을 때  첫번째 암호와 두번째 암호가 일치한지 확인하고 일치하지 않으면 서버로 비밀번호를 전송하지 않도록 만든 코드입니다.
<br>
<br>
<img src="{{site.baseurl}}/images/formEvent3.png" style="width:100%" alt="">
<br>
<img src="{{site.baseurl}}/images/formEvent2.png" style="width:100%" alt="">
<br>
동의버튼을 눌렀을 때, 모든 약관에 동의가 되어있을 때 등록이 되고 약관에 동의가 모두 되어 있지 않을 때는 약관에 동의하라는 팝업창이 뜨게 만드는 버튼 및 코드입니다.
<br>
<p style="border:1px dashed blue; font-size:90%">이렇게 자바스크립트와 HTML의 상호작용은 사용자가 이벤트를 일으켰을 때, 이벤트 핸들에 의해서 이루어지는 것을 알 수 있습니다. 이벤트는 더욱 다양한 형태로 발생하게 되는데 개발자들은 이런 이벤트들을 가로채서 원하는 행위를 하게 됩니다. </p>

<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript BOM</h3>
<br>
<h4> BOM(Browser Object Model) </h4>
브라우저 객체 모델(Browser Object Model)은 자바스크립트가 브라우저와 소통하기 위한 모델입니다. 공식 표준은 아니지만 모든 브라우저 대부분이 자바스크립트 상호작용에 있어 비슷한 메소드와 속성으로 동작하기에 이와 같은 메소드들을 통칭하여 BOM이라고 합니다. BOM은 웹 브라우저 창을 관리할 목적으로 제공되는 객체 모음을 대상으로 하는 모델로써, 자바스크립트 등에서 이를 사용할 수 있습니다. 브라우저 제작사마다 세부사항이 다소 다르게 구현되고 한정적입니다.
<br>
<br>
<h4> 특징 </h4>
웹 브라우저의 윈도우 객체를 대상으로 하는 윈도우 객체 모델의 일정으로 비표준적이나 대부분의 웹브라우저는 Netscape3를 표준처럼 많이 따릅니다. 이를 DOM Level0이라고도 부르며 웹브라우저를 위한 객체 모델의 표준으로 DOM(문서 객체 모델)이 있습니다. BOM의 역할은 웹 브라우저의 버튼, URL 주소 입력 창, 타이틀 바 등 웹브라우저 윈도우 및 웹페이지의 일부분을 제어할 수 있게끔 하는 윈도우 객체 모델입니다.
<br>
<br>
<p style="font-size:110%;"> Window 객체 </p>
<ul>
  <li> window 객체는 모든 브라우저로부터 지원받으며 이는 브라우저의 window를 지칭한다.</li>
  <li> 모든 전역 자바스크립트 객체, 함수, 변수들은 자동적으로 window 객체의 멤버가 됩니다. </li>
  <li> 전역 변수는 window 객체의 속성이 되고 전역 함수는 window 객체의 함수가 됩니다. </li>
  <li> HTML DOM의 Document 객체 역시 window 객체의 속성입니다. </li>
</ul>
~ 지금까지 본 window history, screen 등 이러한 것들을 브라우저 객체 모델(Browser Object Model) BOM 이라고 합니다.

<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript DOM</h3>
<br>
문서 객체 모델(Document Object Model)은 HTML, XML 문서의 프로그래밍 interface입니다. DOM은 문서의 구조화된 표현을 제공하며 프로그래밍 언어가 DOM 구조에 접근할 수 있는 방법을 제공하여 그들의 문서 구조 및 스타일, 내용등을 변경할 수 있게 됩니다. <br>
DOM은 구조화된 node와 property와 method를 갖고 있는 objects로 문서를 표현합니다.
이들은 웹 페이지를 스크립트 또는 프로그래밍 언어들에서 사용될 수 있게 연결시켜주는 역할을 담당합니다.
<br>
<br>
<h4> DOM 선택자</h4>
<h4> 선택자 종류 : 직접선택자, 인접관계 선택자 </h4>
<ol>
  <li>document.getElementByID('아이디명') : id 속성에 해당하는 요소 리턴 </li>
  <li>document.getElementsByClassName('클래스명') : class속성에 해당하는 요소들 리턴(배열형태) </li>
  <li>document.getElementsByTagName('태그명') : 태그명에 해당하는 요소들 리턴(배열형태)
  <hr>
  <li>document.querySelector("선택자") : 선택자에 해당하는 첫번째 요소 리턴 </li>
  <li> document.querySelectorAll("선택자") : 선택자에 해당하는 모든 요소 리턴(배열형태) </li>
<br>

<h3 style="text-align : center; background-color : black; color : white; width:40%; margin:auto;">JavaScript 실습</h3>
<br>
<br>
<iframe src="https://six6929.github.io/BIT_Web/JavaScript/37_js_%EC%9D%B4%EB%B2%A4%ED%8A%B8_%EC%9E%90%EB%8F%99%EC%B0%A8%EA%B2%AC%EC%A0%81(%EC%8B%A4%EC%8A%B5).html" style="width:100%; height:800px;"></iframe>
