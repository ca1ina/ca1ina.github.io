# Vue.js 기초 : 개념<br /><br />
## 사용 이유

- 매우 가볍고 작음 (16kb min+gzip)
- 최고의 런타임 경험 가능<br /><br />

## 세팅<br /><br />
### 링크 삽입<br />
>\<script src="https://unpkg.com/vue/dist/vue.js"></script>
* vue.js의 unpkg 파일을 쓰되, 버전은 쓰지 않아도 무관함<br /><br />

>new Vue({	});
* vue instance로, 화면에 나오는 html 코드와 관련된 vue.js의 템플릿을 제어함<br /><br />

## 개념

### Directive
* Vue.js 라이브러리가 DOM에 작업을 요청하는 markup 
* Vue.js instance가 저장되는 function
* html에 코드 형식으로 기록됨
	* 예) v-bind:href
<br /><br />

## 문법<br /><br />
>el: '#app'
* Connect to DOM 
* html에서 어떤 코드가 vue instance에 의해 제어받는지 설정함
* 문자를 값으로 취함. 보통 id값 표기 방식으로 씀<br /><br />

>data: {  }
* Store data to be used
* object값을 취함<br /><br />

>{{ }}
* Interpolation 혹은 String interpolation으로 불림
* Vue.js는 내부적으로 변수 데이터를 저장하고, html 코드를 기반으로 하여 템플릿을 만들어냄. 이것이 실제 html 코드를 만들어냄.
* {{ }}이 들어간 html 코드를 분석하면 Vue.js 용어는 사라지고, html으로 바뀐 결과만이 나옴
* html내 attribute(="")는 {{ }}문법을 문자로 인식하기 때문에 쓸 수 없음
  
<br />
> v-on:
* Vue.js에게 이 이벤트를 봐 달라고 말하는 역할을 함  
* 템플릿에서 뭔가를 받아달라고 말하는 역할을 함
  * 예) v-on:input, v-on:value 
<br /><br />

> methods: { }
* methods of this vue instance
* 인스턴스들을 보관함. 
* DOM이 갱신될 때 항상 모두 실행됨. Vue.js가 자신 안에 있는 것들을 인식하지 못하기 때문. 
* 데이터의 요소들은 this.***으로 표기함. 
* event는 javascript의 디폴드 이름임.<br /><br />

> computed: { }
* dependent properties
* methods와는 달리 필요할 때만 실행됨. 


> watch: {}
* execute code upon data changes
* 변수의 변화를 추적한 후 명령문을 실행함.
* watch 안의 this는 새로 생성한 vue 전체를 말함 

> v-bind: 
* html attribute에 내용을 지정할 때에는 v-bind를 사용함
* v-bind 뒤에 bind될 html 요소를 적음
  * 예) v-bind:href

> v-once:  
* Vue instance 내의 function 안에서 기존에 있던 변수 값이 재정의될 경우, 그 변수가 들어간 값이 모두 수정된 값으로 동일하게 바뀜.
* v-one는 변수가 한 번만 화면에 출력되도록 함 (re-rendering 불가)  

> v-html
* html 코드로 구성된 데이터를 문자가 아니라 코드로 인식하게 함.  

> v-model
* v-on과 v-bind를 동시에 쓰고 싶을 때 사용
  * data의 변수를 input 필드로 가져오면서, input 필드의 변화가 바로 변수에 저장되게 함 

<br />

## 축약
* v-on: 축약형은 @
* v-bind: 축약형은  :

## Vue.js & javascript

* {{ }} 혹은 methods안에 javascript 코드를 적을 수 있음
  * 예) {{ counter > 10 ? 'Greater than 10' : 'Smaller than 10' }}

