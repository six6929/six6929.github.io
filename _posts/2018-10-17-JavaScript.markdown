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
<iframe src="https://six6929.github.io/DIGB313/Homework7/Homework7.html" style=" width:100%; height:300px; border:1px solid black"></iframe>
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
<pre style="border:2px dotted black">
                  var name = "global";    //전역 변수를 선언
                  function checkscope() {
                      var name = "local"; //지역 변수를 선언
                      console.log(name);  //전역 변수가 아닌 지역 변수를
                  }
                  checkscope();
</pre>
<hr>

<pre style="border:2px dotted black">
                  var name = "global"     // 전역 변수를 선언
                  function checkscope() {
                      name = "local";     //전역 변수를 변경
                      name2 = "local";    //암묵적으로 새 전역 변수가 선언됨
                  }
                  checkscope();
                  console.log(name);      //output: "local"
                  console.log(name2);     //output: "local"
</pre>
