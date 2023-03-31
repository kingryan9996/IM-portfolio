<template>
  <article class="third-area-wrap">
    <div class="third-left">
        <figure>
            <img src="@/assets/img/profile.jpg">
            <figcaption>전자 사인 자리</figcaption>
        </figure>
    </div>
    <div class="third-right">
        <h2>ABOUT ME</h2>
        <h3>SKILL</h3>
        <ul class="third-right-items basic">
            <li class="html"><img src="@/assets/skill-svg/html-5.svg"></li>
            <li class="css"><img src="@/assets/skill-svg/css3.svg"></li>
            <li class="javascript"><img src="@/assets/skill-svg/javascript.svg"></li>
            <li class="git"><img src="@/assets/skill-svg/github.svg"></li>
        </ul>
        <ul class="third-right-items framework">
            <li class="typescript"><figure><img src="@/assets/skill-svg/typescript.svg"><figcaption>기존에 작업하였던 자바스크립트 프로젝트들을 타입스크립트를 활용해 리펙토링 할 수 있습니다.</figcaption></figure></li>
            <li class="react"><figure><img src="@/assets/skill-svg/react.svg"><figcaption>코드의 역할에 따라 컴포넌트를 분리하여 작업할 수 있고 Axios와 React-Query를 사용해 API호출과 상태관리를 할 수 있습니다.</figcaption></figure></li>
            <li class="next"><figure><img src="@/assets/skill-svg/next.svg"><figcaption>기존 CSR방식이 아닌 SEO에 최적화 된 SSR방식의 렌더링을 지원하며, 보다 정적인 사이트인 경우 SSG를 이용해 화면을 제공해줄 수 있습니다.</figcaption></figure></li>
            <li class="vue"><figure><img src="@/assets/skill-svg/vue.svg"><figcaption>기존에 작업하였던 자바스크립트 프로젝트들을 타입스크립트를 활용해 리펙토링 할 수 있습니다.</figcaption></figure></li>
        </ul>
        <h3>FAQ</h3>
        <ul>
            <li>질문 01 : </li>
            <li>질문 01 : </li>
            <li>질문 01 : </li>
        </ul>

    </div>
  </article>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.third-area-wrap {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    margin-bottom: 10%;
    .third-left {
        width: 40%;
        position:sticky;
        top:0;
        figure {
            img {
                width: 100%;
            }
        }
    }
    .third-right {
        width: 60%;
        padding: 5%;
        h2 {
            font-size: 3vw;
            margin-bottom: 2vw;
        }
        h3 {
            font-size: 2vw;
        }
        .third-right-items {
            li {
                img {
                    width: 40px;
                }
            }
        }
        .basic {
            display: flex;
            justify-content: center;
            align-content: center;
            margin: 25px 0 5px;
            li {
                img {
                    width: 50px;
                }                
            }
            .javascript {
                display: flex;                
                flex-wrap: wrap;
                justify-content: center;
                align-content: center;
                    img {
                        width: 40px;
                    }
                }
        }
        .framework {
            margin-bottom: 30px;
            li {
                figure {
                    display: flex;
                    margin: 10px 0;
                    img {
                        margin-right: 10px;
                    }
                    figcaption {
                        text-align: left;
                        font-size: 16px;
                    }
                }
            }
            .vue {
                img {
                    scale: 1.7;
                }
            }
        }
    }
}

</style>