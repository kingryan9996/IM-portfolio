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
        <div class="right-title">
            <h2>ABOUT ME</h2>
            <h3>SKILL</h3>
        </div>
        <ul class="second-right-items framework">
            <li class="html"><figure><img src="@/assets/skill-svg/html-5.svg"><figcaption>각 태그가 가지고 있는 의미에 맞춰 시맨틱한 마크업을 할 수 있습니다.</figcaption></figure></li>
            <li class="css"><figure><img src="@/assets/skill-svg/css3.svg"><figcaption>scss로 css변수 사용 및 depth를 구별하여 스타일을 할 수 있습니다.</figcaption></figure></li>
            <li class="javascript"><figure><img src="@/assets/skill-svg/javascript.svg"><figcaption>DOM요소에 접근하거나 새로운 요소를 생성할 수 있고, 동작원리를 통해 실행코드의 우선순위와 비동기처리를 할 수 있습니다.</figcaption></figure></li>
            <li class="typescript"><figure><img src="@/assets/skill-svg/typescript.svg"><figcaption>인터페이스를 생성해 변수의 타입을 제한할 수 있습니다.</figcaption></figure></li>
            <li class="react"><figure><img src="@/assets/skill-svg/react.svg"><figcaption>코드의 역할에 따라 컴포넌트를 분리하여 작업할 수 있고 Redux와 React-Query를 통해 데이터의 상태관리를 할 수 있습니다.</figcaption></figure></li>
            <li class="next"><figure><img src="@/assets/skill-svg/next.svg"><figcaption>CSR방식이 아닌 SEO에 최적화 된 SSR방식의 렌더링을 지원하며, 보다 정적인 사이트인 경우 SSG를 이용해 화면을 제공해줄 수 있습니다.</figcaption></figure></li>
            <li class="vue"><figure><img src="@/assets/skill-svg/vue.svg"><figcaption>작업하였던 자바스크립트 프로젝트들을 타입스크립트를 활용해 리펙토링 할 수 있습니다.</figcaption></figure></li>
            <li class="git"><figure><img src="@/assets/skill-svg/github.svg"><figcaption>브런치를 활용해 프로젝트의 버전관리를 할 수 있습니다.</figcaption></figure></li>
        </ul>
    </div>
  </article>
</template>

<script>
export default {
    data() {
        return {
            kww:""
        }
    },
    mounted() {

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
    padding: 0 220px 10%;
    position: relative;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;    
    .second-left {
        width: 40%;
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
        padding: 5% 0 5% 5%;
        transform: translateY(15%);
        .right-title {
            h2 {
                font-size: 3vw;
                margin-bottom: 2vw;
            }
            h3 {
                font-size: 2vw;
            }
        }
        .second-right-items {
            li {
                margin-bottom: 0.2vw;
                text-align: center;
                border-radius: 16px;
                padding: 0.7vw;
                &:hover {
                    cursor: url('https://res.cloudinary.com/dvkugaw3b/image/upload/v1641562029/cursor-worm_kij6gi.png');
                    // background-color:#F2EFE8;
                    transition: 0.5s;
                }
                figure {
                    display: flex;
                    justify-content: flex-start;
                    align-items: center;
                    img {
                        width: 2.2vw;
                        margin: 0 1vw 0 0.5vw;
                    }
                    figcaption {
                        text-align: left;
                        font-size: 0.9vw;
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
            .html:hover {
                    background-color: rgba(230, 81, 0, 0.01);
                    box-shadow: 5px 5px 8px rgba(230, 81, 0, 0.3);
                }
            .css:hover, .typescript:hover {
                background-color: rgba(192, 230, 248, 0.08);
                    box-shadow: 5px 5px 8px rgba(192, 230, 248, 0.9);
                }
            .javascript:hover {
                background-color: rgba(247, 223, 30, 0.01);
                    box-shadow: 5px 5px 8px rgba(247, 223, 30, 0.4);
                }
            .react:hover {
                background-color: rgba(97, 218, 251, 0.01);
                    box-shadow: 5px 5px 8px rgba(97, 218, 251, 0.3);
                }
            .next:hover, .git:hover {
                background-color: rgba(0, 0, 0, 0.01);
                    box-shadow: 5px 5px 8px rgba(0, 0, 0, 0.15);
                }
            .vue:hover {
                background-color: rgba(65, 184, 131, 0.01);
                    box-shadow: 5px 5px 8px rgba(65, 184, 131, 0.3);
                }
        }
    }
}

</style>