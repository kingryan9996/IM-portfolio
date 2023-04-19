<template>
    <article class="second-area-wrap">
        <div class="second-left">
          <div class="section-01">
              <div class="section-number">01</div>
              <div class="section-title">
                  <span>ABOUT ME</span>
              </div>
          </div>
          <div class="my-photo">
              <img src="@/assets/img/profile.png">
              <img class="my-sign" src="@/assets/img/sign1.svg"/>
          </div>
          <div class="photo-right">
            <ul>
                <li><p>Name : 임승환</p></li>
                <li><p>Birth : 1994.01.29</p></li>
                <li><p>Address : 서울시 관악구</p></li>
                <li><p>Email : kingryan9996@gmail.com</p></li>            
            </ul>
            <p><strong>저를 소개하자면</strong><br/>
            문제가 발생하면 잠시 물러납니다.<br/>
            실수로 놓치고 있던 것들을 탐색하고<br/>
            필요한 방법을 검색해서 다시 접근합니다.<br/>
            저는 이렇게 문제를 해결하는 개발자입니다.
            </p>
        </div>          
      </div>
      <div class="second-right">
          <div class="about-intro">
              <div class="intro-first">                
                  <p>
                    문제가 발생하면 잠시 물러납니다.<br/>
                  실수로 놓치고 있던 것들을 탐색하고<br/>
                  필요한 방법을 검색해서 다시 접근합니다.<br/>
                  저는 이렇게 문제를 해결하는 개발자입니다.
                  </p>
                  <div class="intro-right">
                      <img src="@/assets/img/icons8-나는-여기있다.-48.png">
                      <img src="@/assets/img/student-64.png">
                      <!-- <span>반갑습니다!</span> -->
                  </div>
              </div>
              <p class="intro-main">
                   저는 비전공자로 다른업종에 종사하다 2022년 8월 새로운 도전을 위해 IT세계에 뛰어 들었습니다.
                  코딩을 접한지 6개월에 다다르고 있지만, 저의 흥미와 열정은 날로 늘어가고 있습니다.
                  공부하면 할수록 일맥상통해가는 프로그래밍의 세계에 흥미를 느껴 최근에는 좀 더 폭넓은 개념을 익히기 위해
                  프론트엔드 언어뿐만이 아닌, Java와 Spring프레임워크도 공부하고있습니다.
                  이렇듯 저는 말 그대로 의욕이 넘쳐나는 신입의 자세로 업무에 임할 준비가 되어있습니다.
              </p>
          </div>
          <div class="about-skill">
              <h3>SKILL</h3>
              <ul class="second-right-items">
                  <li class="html" data-tooltip="html"><figure><img src="@/assets/skill-svg/html-5.svg"><figcaption>각 태그가 가지고 있는 의미에 맞춰 시맨틱한 마크업을 할 수 있습니다.</figcaption></figure></li>
                  <li class="css" data-tooltip="css"><figure><img src="@/assets/skill-svg/css3.svg"><figcaption>scss를 통해 변수를 활용하여 스타일 할 수 있습니다.</figcaption></figure></li>
                  <li class="javascript" data-tooltip="javascript"><figure><img src="@/assets/skill-svg/javascript.svg"><figcaption>DOM요소에 접근하거나 새로운 요소를 생성할 수 있고, 동작원리를 통해 실행코드의 우선 순위 설정과 비동기처리를 할 수 있습니다.</figcaption></figure></li>
                  <li class="typescript" data-tooltip="typescript"><figure><img src="@/assets/skill-svg/typescript.svg"><figcaption>인터페이스를 생성해 변수의 타입을 제한할 수 있습니다.</figcaption></figure></li>
                  <li class="react" data-tooltip="react"><figure><img src="@/assets/skill-svg/react.svg"><figcaption>코드의 역할에 따라 컴포넌트를 분리하여 작업할 수 있고 Redux와 React-Query를 통해 데이터의 상태관리를 할 수 있습니다.</figcaption></figure></li>
                  <li class="next" data-tooltip="next"><figure><img src="@/assets/skill-svg/next.svg"><figcaption>CSR방식이 아닌 SEO에 최적화 된 SSR방식의 렌더링을 지원하며, 보다 정적인 사이트인 경우 SSG를 이용해 화면을 제공해줄 수 있습니다.</figcaption></figure></li>
                  <li class="vue" data-tooltip="vue"><figure><img src="@/assets/skill-svg/vue.svg"><figcaption>작업하였던 자바스크립트 프로젝트들을 타입스크립트를 활용해 리펙토링 할 수 있습니다.</figcaption></figure></li>
                  <li class="git" data-tooltip="git"><figure><img src="@/assets/skill-svg/github.svg"><figcaption>브런치를 활용해 프로젝트의 버전관리를 할 수 있습니다.</figcaption></figure></li>
              </ul>
              <h3 class="right-used-title">USED</h3>
              <ul class="second-right-used">
                  <li v-for="(item,index) in usedList" :key="index" :class="item" :data-tooltip="item"><img :src="require(`@/assets/skill-used/${item}.png`)"></li>
              </ul>
          </div>
      </div>
    </article>
  </template>
  
  <script>
  export default {
      data() {
          return {
              usedList: [
                "axios","bootstrap","esLint","express","figma","framer","java","jQuery","mariadb","MUI","mySQL","netlify","NextAuth","node.js","react-query","react-router","simple-maps","redux","sass","spring","swiper"
              ]
          }
      },
      mounted() {

        console.log(this.usedList)
        console.log(this.usedList[0])
        console.log(this.usedList[1])
        // this.usedList.push()
        
  
          const getSec02Height = () => {
  
              const leftSide01Div = document.querySelector(".second-left > .section-01")
              const leftSideImg = document.querySelector(".second-left > .my-photo > img")
              const chapterBorder = document.querySelector(".chapterBorder01")
  
              // console.log(leftSideImg.clientHeight)
              
              
              if (matchMedia("screen and (max-width: 534px)").matches) {
                  leftSide01Div.style = `
                  height: ${leftSideImg.clientHeight * 2.5 }px`
                } else {                    
                    leftSide01Div.style = `
                    height: ${leftSideImg.clientHeight * 0.9 }px`
                }
  
              
              // padding-top: ${workList[0].clientHeight / 5}px;
              // margin-bottom: ${workList[0].clientHeight / 2}px`;
              chapterBorder.style = `
              position: absolute;
              border-top: 1px solid #000;
              width: ${leftSideImg==true?(leftSideImg.clientHeight / 2.2):120}px;
              top: 50%;
              left: 110%;
              transform: translateY(-50%);`
          }
  
          window.addEventListener("load",()=>{
              const secChapterWrap = document.querySelector(".section-01 > .section-title ")
              const secChapter = document.createElement("div")
              secChapterWrap.appendChild(secChapter)
              secChapter.classList.add("chapterBorder01")
  
              getSec02Height();
          })
          window.addEventListener('resize',()=>{
              getSec02Height();
          })
  
      }
  
  }
  </script>
  
  <style lang="scss">
@import "@/assets/scss/secondArea.scss";  
  </style>