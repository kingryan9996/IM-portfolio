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
              <img src="@/assets/img/profile.jpg">
              <img class="my-sign" src="@/assets/img/sign1.svg"/>
          </div>
      </div>
      <div class="second-right">
          <div class="about-intro">
              <div class="intro-first">                
                  <p>
                    저는 문제가 발생하면 한 발짝 뒤로 물러나<br/>
                  전체적인 데이터의 흐름과 원인을 파악하고<br/>
                  문제 해결에 필요한 모든 방법을 동원하여<br/>
                  어떻게든 해결방법을 찾아내는 개발자입니다.
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
                  <li class="html"><figure><img src="@/assets/skill-svg/html-5.svg"><figcaption>각 태그가 가지고 있는 의미에 맞춰 시맨틱한 마크업을 할 수 있습니다.</figcaption></figure></li>
                  <li class="css"><figure><img src="@/assets/skill-svg/css3.svg"><figcaption>scss로 css변수 사용 및 depth를 구별하여 스타일을 할 수 있습니다.</figcaption></figure></li>
                  <li class="javascript"><figure><img src="@/assets/skill-svg/javascript.svg"><figcaption>DOM요소에 접근하거나 새로운 요소를 생성할 수 있고, 동작원리를 통해 실행코드의 우선 순위 설정과 비동기처리를 할 수 있습니다.</figcaption></figure></li>
                  <li class="typescript"><figure><img src="@/assets/skill-svg/typescript.svg"><figcaption>인터페이스를 생성해 변수의 타입을 제한할 수 있습니다.</figcaption></figure></li>
                  <li class="react"><figure><img src="@/assets/skill-svg/react.svg"><figcaption>코드의 역할에 따라 컴포넌트를 분리하여 작업할 수 있고 Redux와 React-Query를 통해 데이터의 상태관리를 할 수 있습니다.</figcaption></figure></li>
                  <li class="next"><figure><img src="@/assets/skill-svg/next.svg"><figcaption>CSR방식이 아닌 SEO에 최적화 된 SSR방식의 렌더링을 지원하며, 보다 정적인 사이트인 경우 SSG를 이용해 화면을 제공해줄 수 있습니다.</figcaption></figure></li>
                  <li class="vue"><figure><img src="@/assets/skill-svg/vue.svg"><figcaption>작업하였던 자바스크립트 프로젝트들을 타입스크립트를 활용해 리펙토링 할 수 있습니다.</figcaption></figure></li>
                  <li class="git"><figure><img src="@/assets/skill-svg/github.svg"><figcaption>브런치를 활용해 프로젝트의 버전관리를 할 수 있습니다.</figcaption></figure></li>
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
              leftSide01Div.style = `
              height: ${leftSideImg.clientHeight * 0.9 }px`
  
              
              // padding-top: ${workList[0].clientHeight / 5}px;
              // margin-bottom: ${workList[0].clientHeight / 2}px`;
              chapterBorder.style = `
              position: absolute;
              border-top: 1px solid #000;
              width: ${leftSideImg.clientHeight / 2.2}px;
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
  .second-area-wrap {
      padding: 0 11.5% 10%;
      position: relative;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: flex-start;
      .second-left {
          width: 40%;        
          margin-top: 5.5vw;
          padding-left: 10%;
          padding-top: 6vw;
          position:sticky;
          top:10%;
          .section-01 {
              // height: 100%;
              position: absolute;
              top: 16%;
              left: -12%;
              display: flex;
              flex-direction: column;
              justify-content: space-between;
              align-content: center;
          .section-number {
              font-size: 4vw;
              font-weight: 700;
              position: static;
              background-color: #FFF;
              z-index: 1;
          }
          .section-title {
              position:relative;
              transform: rotateZ(270deg);
              font-size: 1.6vw;
              font-weight: 400;
          }
      }        
          .my-photo {
              position: relative;
              z-index: 2;
              img {
                  width: 100%;
              }
              .my-sign {
                  position: absolute;
                  bottom: 0;
                  right: 0;
                  transform: translate(100%,100%);
                  scale: 0.3;
              }
          }
      }
      .second-right {
          width: 60%;
          margin-bottom: 7%;
          padding: 2.5% 0 5% 5%;
          transform: translateY(15%);
              h3 {
                  font-size: 2vw;
                  font-weight: 500;
              }
              .about-intro {                
                  margin-bottom: 3vw;
                  .intro-first {
                      display: flex;
                      justify-content: space-between;
                      align-items: center;
                      .intro-right {                        
                          display:flex;
                          flex-direction: column;
                          justify-content: center;
                          align-items: center;
                          margin-right:2vw;
                          transform: translateY(-10%);
                          img {
                              width: 4vw;
                          }
                          span {
                              font-size: 1.2vw;
                              margin-top: 0.25vw;
                          }
                      }
                      p {
                          // text-align: right;
                          text-align: left;
                          font-size: 1.6vw;
                          line-height: 2vw;                        
                          // font-size: 1.4vw;
                          // line-height: 2vw;
                      }
                  }
                  .intro-main {
                      margin-top: 0.9vw;
                      text-align: left;
                      font-size: 0.9vw;
                      line-height: 1.5vw;
                      color: #555;
                  }
              }
              .about-skill {
                  h3 {
                      text-align: left;
                      margin-bottom: 0.7vw;
                  }
                  .second-right-items {
                    margin-bottom: 3vw;
                          li {
                              margin-bottom: 0.2vw;
                              border-radius: 16px;
                              padding: 0.4vw;
                              transform: translateX(-0.4vw);
                              color: #555;
                              figure {
                                  display: flex;
                                  justify-content: flex-start;
                                  align-items: center;                                                                  
                                  img {
                                      width: 2vw;
                                      margin: 0 1vw 0 0;
                                  }
                                  figcaption {
                                      text-align: left;
                                      font-size: 0.9vw;
                                      &::after {
                                        display: inline-block;
                                        content: "";
                                        width: 0;
                                        height: 0;
                                        border-bottom: 0.4vw solid transparent;
                                        border-top: 0.4vw solid transparent;
                                        border-left: 0.5vw solid transparent;
                                        border-right: 0.6vw solid transparent;
                                        border-radius: 1.2px;
                                        transition: 0.25s;
                                        }
                                  }
                              }
                          }
                          .html, .css {
                              img {
                                  scale: 1.3;
                              }
                          }
                          .vue {
                              img {
                                  scale: 1.7;
                              }
                          }
                          .git {
                              img {
                                  scale: 1.2;
                              }
                          }
                          .html:hover > figure > figcaption::after {                            
                              border-right-color: rgba(230, 81, 0, 0.8);
                              // background-color: rgba(230, 81, 0, 0.01);
                              // box-shadow: 5px 5px 8px rgba(230, 81, 0, 0.3);
                              }
                          .css:hover > figure > figcaption::after, .typescript:hover > figure > figcaption::after {                            
                              border-right-color: rgba(2, 119, 189, 0.8);
                              // background-color: rgba(192, 230, 248, 0.08);
                              // box-shadow: 5px 5px 8px rgba(192, 230, 248, 0.9);
                              }
                          .javascript:hover > figure > figcaption::after {                            
                              // border-right-color: rgba(247, 223, 30, 1);
                              border-right-color: rgba(250, 200, 17, 1);
                              // background-color: rgba(247, 223, 30, 0.01);
                              // box-shadow: 5px 5px 8px rgba(247, 223, 30, 0.4);
                              }
                          .react:hover > figure > figcaption::after {                            
                              border-right-color: rgba(97, 218, 251, 0.9);
                            //   background-color: rgba(97, 218, 251, 0.01);
                            //   box-shadow: 5px 5px 8px rgba(97, 218, 251, 0.3);
                              }
                          .next:hover > figure > figcaption::after, .git:hover > figure > figcaption::after {                            
                              border-right-color: rgba(0, 0, 0, 0.6);
                            //   background-color: rgba(0, 0, 0, 0.01);
                            //   box-shadow: 5px 5px 8px rgba(0, 0, 0, 0.15);
                              }
                          .vue:hover > figure > figcaption::after {                            
                              border-right-color: rgba(65, 184, 131, 0.8);
                            //   background-color: rgba(65, 184, 131, 0.01);
                            //   box-shadow: 5px 5px 8px rgba(65, 184, 131, 0.3);
                              }
                    }                    
                    .second-right-used {
                        display: flex;
                        flex-wrap: wrap;
                        position: relative;
                        li {
                            padding: 0.4vw;
                            position: relative;
                            opacity: 0.6;
                            // transition: 0.3s;
                            border-radius: 50%;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            &:hover {
                                opacity: 1;
                                box-shadow: 0.2px 0.2px 35px rgba(0, 0, 0, 0.2);
                            }
                            &::before,&::after {
                                z-index: 99;
                            }
                            &:hover::before {
                                content: "";
                                display: block;
                                width: 0;
                                height: 0;
                                border-bottom: 0.3vw solid black;
                                border-top: 0.3vw solid transparent;
                                border-left: 0.3vw solid transparent;
                                border-right: 0.3vw solid transparent;
                                border-radius: 1.2px;
                                position: absolute;
                                bottom: 0;
                                left: 50%;
                                transform: translate(-50%, 70%);
                                // transition: 0.5s;
                            }
                            &:hover:after{
                                content: attr(data-tooltip);
                                display: block;
                                text-align: center;
                                background-color: #000;
                                color:#fff;
                                padding:0.25vw 0.6vw;
                                white-space: nowrap;
                                font-size:0.5vw;
                                position: absolute;
                                bottom: 0%;
                                left: 50%;
                                transform: translate(-50%, 130%);
                                border-radius: 40px;
                                text-transform: capitalize;
                            }
                            img {
                                width: 2vw;
                                height: 2vw;
                            }
                        }
                        .axios > img {
                            scale: 1.2;
                        }
                        .figma, .framer, .NextAuth {
                            img {
                                scale: 0.8;
                                transform: translateY(5%);
                            }
                        }
                        .netlify, .react-query {
                            img {
                                scale: 0.9;
                            }
                        }
                        .express, .jQuery, .swiper {
                            img {
                                scale: 0.83;
                            }
                        }
                        .react-router , .redux {
                            img {
                                scale: 0.9;
                                transform: translateY(-5%);
                            }
                        }
                    }
              }
          
      }
  }
  
  </style>