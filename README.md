# :pushpin: (리액트) 향수 쇼핑몰
>향수 쇼핑몰 컨셉의 사이트를 리액트로 구현했습니다

>https://irrpl-ar.github.io/React_Winter-perfume

</br>

## 1. 제작 기간 & 참여 인원
- 2021년 12월 3일
- 개인 프로젝트

</br>

## 2. 사용 기술
#### `Front-end`
  - React JS
  - Jsx
  - CSS

</br>

## 3. 핵심 기능

<details>
<summary><b>핵심 기능 설명 펼치기</b></summary>
<div markdown="1">

### SPA
- 쇼핑몰 컨셉으로 싱글 페이지 어플리케이션을 구현하였습니다   
- 맨 처음 메인 페이지와 캐러셀, 상품들이 뜨고 상단 메뉴바를 클릭하면   
 각 상품 소개 상세 페이지로 연결했습니다

### useState, useEffect
- useState와 useEffect를 사용하여 동적인 기능을 구현했습니다

</div>
</details>

</br>

## 4. 디버깅
### 4-1. 핵심 디버깅

```각 상품들을 map으로 반복시 사진이 저장된 변수가 반복이 안되는 문제```

* 이전에 map으로 반복시에 이미지 src가 주소로 연결이 되었을 때는 문제가 없었는데   
이번에는 로컬에 저장된 사진을 변수에 담아 import하니 반복시 에러가 남
* console.log 검사를 해보니, {변수} 일 때는 문제가 없는데 {변수}+props.i 나   
백틱 등으로 결합해서 사용하려했을 때 결국 img src="perfume0" 이런식으로 문자처럼 인식이 됨
* src 주소를 데이터 객체에 넣어도 보고, 다양하게 시도해봤으나 계속 오류가 해결이 안됨
* 구글링 끝에 ```<img src={ require('../img/perfume' + props.i + '.jpg').default } alt=""/>``` 이렇게   
require와 default를 사용하여 했을 때 이미지까지 map 반복이 잘됨

</br>


### 4-2. 각종 디버깅
<details>
<summary>라우터 Link 사용시 문제</summary>
<div markdown="1">

```
<span Link to ="/">Home </span>
```

* 실수로 span 태그 안에 Link 를 넣어서 작동 안됨
* ```<Link to ="/"> <span>Home </span> </Link>``` 로 해결


</details>

</br>

## 5. 회고 / 느낀점
> 리액트를 배우고 처음으로 개인 프로젝트를 만들어서 뿌듯하다   
사실 정말 별거 아닌 기능이지만, Router문제도 해결하고 useState도 써보니 좋았다   
버전 문제로 인한 오류 해결에 시간을 많이 허비한게 아쉽지만, 그 과정 중에  
공식 문서나 구글링으로 공부가 된 것 같다


