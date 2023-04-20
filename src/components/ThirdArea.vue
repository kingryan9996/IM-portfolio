<template>
  <article class="third-area-wrap">
    <div class="third-left">
        <div class="section-02">
            <div class="section-number">02</div>
            <div class="section-title">
                <span>PROJECT</span>
            </div>
        </div>
        <div class="work-description" ref="workDescription">
            <h3 v-html="workTitle"></h3>
            <p v-html="workIntroduction"></p>
            <div class="link-wrap" ref="linkWrap">
                <a class="work-github" ref="workGithub" target="_blank" href="">
                    <svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 30 30" width="48px" height="48px" fill="#FFF"><path d="M15,3C8.373,3,3,8.373,3,15c0,5.623,3.872,10.328,9.092,11.63C12.036,26.468,12,26.28,12,26.047v-2.051 c-0.487,0-1.303,0-1.508,0c-0.821,0-1.551-0.353-1.905-1.009c-0.393-0.729-0.461-1.844-1.435-2.526 c-0.289-0.227-0.069-0.486,0.264-0.451c0.615,0.174,1.125,0.596,1.605,1.222c0.478,0.627,0.703,0.769,1.596,0.769 c0.433,0,1.081-0.025,1.691-0.121c0.328-0.833,0.895-1.6,1.588-1.962c-3.996-0.411-5.903-2.399-5.903-5.098 c0-1.162,0.495-2.286,1.336-3.233C9.053,10.647,8.706,8.73,9.435,8c1.798,0,2.885,1.166,3.146,1.481C13.477,9.174,14.461,9,15.495,9 c1.036,0,2.024,0.174,2.922,0.483C18.675,9.17,19.763,8,21.565,8c0.732,0.731,0.381,2.656,0.102,3.594 c0.836,0.945,1.328,2.066,1.328,3.226c0,2.697-1.904,4.684-5.894,5.097C18.199,20.49,19,22.1,19,23.313v2.734 c0,0.104-0.023,0.179-0.035,0.268C23.641,24.676,27,20.236,27,15C27,8.373,21.627,3,15,3z"/></svg>
                    <span>깃허브 링크</span>
                </a>
                <a class="work-link" ref="workLink" target="_blank" href="">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 30 31" width="48px" height="48px" fill="#000">
                        <g>
                            <path d="M21.25 15.9136C21.25 19.3654 18.4518 22.1636 15 22.1636C11.5482 22.1636 8.75 19.3654 8.75 15.9136C8.75 12.4618 11.5482 9.66357 15 9.66357C18.4518 9.66357 21.25 12.4618 21.25 15.9136Z" stroke="#FFF" stroke-width="1.5"></path>
                            <path d="M12.5 9.91357C12.5 9.91357 17 15.4136 18 21.4136" stroke="#FFF" stroke-width="1.5"></path>
                            <path d="M19.5 11.9136C19.5 11.9136 14.5 15.9136 8.5 16.9136" stroke="#FFF" stroke-width="1.5"></path>
                            <path d="M12 21.4137C12 21.4137 15.5 16.4137 21.5 17.4137" stroke="#FFF" stroke-width="1.5"></path>
                        </g>
                    </svg>
                    <span>배포사이트</span>
                </a>
            </div>
        </div>
    </div>
    <div class="third-right">        
        <ul class="third-right-items">
            <li><img src="@/assets/img/GiftTree.png">
                <div class="mobile-description">
                    <h3>선물트리</h3>
                    <p>친구끼리 선물주고받기</p>
                    <div class="link-wrap">
                        <a class="work-github" target="_blank" href="https://github.com/kingryan9996/greengift-next">
                            <svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 30 30" width="48px" height="48px" fill="#FFF"><path d="M15,3C8.373,3,3,8.373,3,15c0,5.623,3.872,10.328,9.092,11.63C12.036,26.468,12,26.28,12,26.047v-2.051 c-0.487,0-1.303,0-1.508,0c-0.821,0-1.551-0.353-1.905-1.009c-0.393-0.729-0.461-1.844-1.435-2.526 c-0.289-0.227-0.069-0.486,0.264-0.451c0.615,0.174,1.125,0.596,1.605,1.222c0.478,0.627,0.703,0.769,1.596,0.769 c0.433,0,1.081-0.025,1.691-0.121c0.328-0.833,0.895-1.6,1.588-1.962c-3.996-0.411-5.903-2.399-5.903-5.098 c0-1.162,0.495-2.286,1.336-3.233C9.053,10.647,8.706,8.73,9.435,8c1.798,0,2.885,1.166,3.146,1.481C13.477,9.174,14.461,9,15.495,9 c1.036,0,2.024,0.174,2.922,0.483C18.675,9.17,19.763,8,21.565,8c0.732,0.731,0.381,2.656,0.102,3.594 c0.836,0.945,1.328,2.066,1.328,3.226c0,2.697-1.904,4.684-5.894,5.097C18.199,20.49,19,22.1,19,23.313v2.734 c0,0.104-0.023,0.179-0.035,0.268C23.641,24.676,27,20.236,27,15C27,8.373,21.627,3,15,3z"/></svg>
                            <span>깃허브 링크</span>
                        </a>
                        <a class="work-link" target="_blank" href="https://port-0-next-greengift-nx562olfqkxd9g.sel3.cloudtype.app/">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 30 31" width="48px" height="48px" fill="#000">
                                <g>
                                    <path d="M21.25 15.9136C21.25 19.3654 18.4518 22.1636 15 22.1636C11.5482 22.1636 8.75 19.3654 8.75 15.9136C8.75 12.4618 11.5482 9.66357 15 9.66357C18.4518 9.66357 21.25 12.4618 21.25 15.9136Z" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M12.5 9.91357C12.5 9.91357 17 15.4136 18 21.4136" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M19.5 11.9136C19.5 11.9136 14.5 15.9136 8.5 16.9136" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M12 21.4137C12 21.4137 15.5 16.4137 21.5 17.4137" stroke="#FFF" stroke-width="1.5"></path>
                                </g>
                            </svg>
                            <span>배포사이트</span>
                        </a>
                    </div>
                </div>
            </li>            
            <li><img src="https://i.pinimg.com/564x/56/15/dd/5615dde0afe82cd720b1a7d85d233d9d.jpg">
            <div class="mobile-description">
                    <h3>Japan Travel</h3>
                    <p>일본여행을 계획중인 유저들을 위한 일본의 대표 관광지 소개 사이트</p>
                    <div class="link-wrap">
                        <a class="work-github" target="_blank" href="https://github.com/japan-travel-planner/japan-travel-planner">
                            <svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 30 30" width="48px" height="48px" fill="#FFF"><path d="M15,3C8.373,3,3,8.373,3,15c0,5.623,3.872,10.328,9.092,11.63C12.036,26.468,12,26.28,12,26.047v-2.051 c-0.487,0-1.303,0-1.508,0c-0.821,0-1.551-0.353-1.905-1.009c-0.393-0.729-0.461-1.844-1.435-2.526 c-0.289-0.227-0.069-0.486,0.264-0.451c0.615,0.174,1.125,0.596,1.605,1.222c0.478,0.627,0.703,0.769,1.596,0.769 c0.433,0,1.081-0.025,1.691-0.121c0.328-0.833,0.895-1.6,1.588-1.962c-3.996-0.411-5.903-2.399-5.903-5.098 c0-1.162,0.495-2.286,1.336-3.233C9.053,10.647,8.706,8.73,9.435,8c1.798,0,2.885,1.166,3.146,1.481C13.477,9.174,14.461,9,15.495,9 c1.036,0,2.024,0.174,2.922,0.483C18.675,9.17,19.763,8,21.565,8c0.732,0.731,0.381,2.656,0.102,3.594 c0.836,0.945,1.328,2.066,1.328,3.226c0,2.697-1.904,4.684-5.894,5.097C18.199,20.49,19,22.1,19,23.313v2.734 c0,0.104-0.023,0.179-0.035,0.268C23.641,24.676,27,20.236,27,15C27,8.373,21.627,3,15,3z"/></svg>
                            <span>깃허브 링크</span>
                        </a>
                        <a class="work-link" target="_blank" href="https://japan-travel-planner.github.io/japan-travel-planner">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 30 31" width="48px" height="48px" fill="#000">
                                <g>
                                    <path d="M21.25 15.9136C21.25 19.3654 18.4518 22.1636 15 22.1636C11.5482 22.1636 8.75 19.3654 8.75 15.9136C8.75 12.4618 11.5482 9.66357 15 9.66357C18.4518 9.66357 21.25 12.4618 21.25 15.9136Z" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M12.5 9.91357C12.5 9.91357 17 15.4136 18 21.4136" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M19.5 11.9136C19.5 11.9136 14.5 15.9136 8.5 16.9136" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M12 21.4137C12 21.4137 15.5 16.4137 21.5 17.4137" stroke="#FFF" stroke-width="1.5"></path>
                                </g>
                            </svg>
                            <span>배포사이트</span>
                        </a>
                    </div>
                </div>
            </li>
            <li><img src="@/assets/img/JapanTravel.png">
            <div class="mobile-description">
                    <h3>Japan Travel</h3>
                    <p>일본여행을 계획중인 유저들을 위한 일본의 대표 관광지 소개 사이트</p>
                    <div class="link-wrap">
                        <a class="work-github" target="_blank" href="https://github.com/japan-travel-planner/japan-travel-planner">
                            <svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 30 30" width="48px" height="48px" fill="#FFF"><path d="M15,3C8.373,3,3,8.373,3,15c0,5.623,3.872,10.328,9.092,11.63C12.036,26.468,12,26.28,12,26.047v-2.051 c-0.487,0-1.303,0-1.508,0c-0.821,0-1.551-0.353-1.905-1.009c-0.393-0.729-0.461-1.844-1.435-2.526 c-0.289-0.227-0.069-0.486,0.264-0.451c0.615,0.174,1.125,0.596,1.605,1.222c0.478,0.627,0.703,0.769,1.596,0.769 c0.433,0,1.081-0.025,1.691-0.121c0.328-0.833,0.895-1.6,1.588-1.962c-3.996-0.411-5.903-2.399-5.903-5.098 c0-1.162,0.495-2.286,1.336-3.233C9.053,10.647,8.706,8.73,9.435,8c1.798,0,2.885,1.166,3.146,1.481C13.477,9.174,14.461,9,15.495,9 c1.036,0,2.024,0.174,2.922,0.483C18.675,9.17,19.763,8,21.565,8c0.732,0.731,0.381,2.656,0.102,3.594 c0.836,0.945,1.328,2.066,1.328,3.226c0,2.697-1.904,4.684-5.894,5.097C18.199,20.49,19,22.1,19,23.313v2.734 c0,0.104-0.023,0.179-0.035,0.268C23.641,24.676,27,20.236,27,15C27,8.373,21.627,3,15,3z"/></svg>
                            <span>깃허브 링크</span>
                        </a>
                        <a class="work-link" target="_blank" href="https://japan-travel-planner.github.io/japan-travel-planner">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 30 31" width="48px" height="48px" fill="#000">
                                <g>
                                    <path d="M21.25 15.9136C21.25 19.3654 18.4518 22.1636 15 22.1636C11.5482 22.1636 8.75 19.3654 8.75 15.9136C8.75 12.4618 11.5482 9.66357 15 9.66357C18.4518 9.66357 21.25 12.4618 21.25 15.9136Z" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M12.5 9.91357C12.5 9.91357 17 15.4136 18 21.4136" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M19.5 11.9136C19.5 11.9136 14.5 15.9136 8.5 16.9136" stroke="#FFF" stroke-width="1.5"></path>
                                    <path d="M12 21.4137C12 21.4137 15.5 16.4137 21.5 17.4137" stroke="#FFF" stroke-width="1.5"></path>
                                </g>
                            </svg>
                            <span>배포사이트</span>
                        </a>
                    </div>
                </div>
            </li>
        </ul>
    </div>
  </article>
</template>

<script>
export default {
    data() {
        return {
            workTitle:"",
            workIntroduction:""            
        }
    },
    mounted() {

        const thirdSec = document.querySelector(".third-area-wrap")
        const workList = document.querySelectorAll(".third-right-items > li")

        // document.querySelector(".third-left").style["padding-bottom"] = `${ (workList[1].clientHeight / 100 ) * 60 }px`;

        // console.log(workList)
        // console.log(workList[0].clientHeight)
        // console.log(thirdSec.offsetTop + workList[0].offsetTop)
        // console.log(thirdSec.offsetTop + workList[1].offsetTop)
        // console.log(thirdSec.offsetTop + workList[2].offsetTop)


        // console.log(document.querySelector(".third-left > h2"))


        document.addEventListener('scroll',()=>{

                if ( window.pageYOffset >= 0 && ( window.pageYOffset < thirdSec.offsetTop + workList[0].offsetTop ) ){
                    this.workTitle = "MY PROJECT"
                    this.workIntroduction = ""
                    this.$refs.workGithub.href = ""
                    this.$refs.workLink.href = ""
                } else if ( window.pageYOffset > ( thirdSec.offsetTop + workList[0].offsetTop ) && ( window.pageYOffset < thirdSec.offsetTop + workList[1].offsetTop ) ){
                    this.workTitle = "첫번째 작품"
                    this.workIntroduction = "첫번째~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~"
                    this.$refs.workGithub.href = ""
                    this.$refs.workLink.href = ""
                } else if ( window.pageYOffset > ( thirdSec.offsetTop + workList[1].offsetTop ) && ( window.pageYOffset < thirdSec.offsetTop + workList[2].offsetTop ) ){
                    this.workTitle = "두번째 작품"
                    this.workIntroduction = "두번쨰~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~"
                    this.$refs.workGithub.href = ""
                    this.$refs.workLink.href = ""
                } else if ( window.pageYOffset > ( thirdSec.offsetTop + workList[2].offsetTop ) ){
                    this.workTitle = "Japan Travel"
                    this.workIntroduction = "일본여행을 계획중인 유저들을 위한 일본의 대표 관광지 소개 사이트"
                    this.$refs.workGithub.href = "https://github.com/japan-travel-planner/japan-travel-planner"
                    this.$refs.workLink.href = "https://japan-travel-planner.github.io/japan-travel-planner/"
                }

                linkWrapVis();
            }
        )

        const getSec03Height = () => {

            const leftSide02Div = document.querySelector(".third-left")
            const chapterBorder = document.querySelector(".chapterBorder02")
            const rightSideListItem = document.querySelectorAll(".third-right-items > li > img")

            leftSide02Div.style = `
            height: ${workList[0].clientHeight}px;
            padding-top: ${workList[0].clientHeight / 5}px;
            margin-bottom: ${workList[0].clientHeight * 0.1}px`;

            console.log(this.$refs.workDescription)
            this.$refs.workDescription.style["height"] = `${workList[0].clientHeight}px`

            // console.log(leftSide02Div)
            chapterBorder.style = `
            position: absolute;
            border-top: 1px solid #FFF;
            width: ${leftSide02Div.clientHeight / 1.6}px;
            top: 50%;
            left: 110%;
            transform: translateY(-50%);`;

            rightSideListItem.forEach(obj => {
                obj.style["height"] = `${obj.clientWidth * 0.65}px`
            })

        }

        const linkWrapVis = () => {
            if (this.workIntroduction == "") {
                this.$refs.linkWrap.style = "display:none"
            } else {
                this.$refs.linkWrap.style = "display:block"
            }
        }

        window.addEventListener("load",()=>{
            const secChapterWrap = document.querySelector(".section-02 > .section-title ")
            const secChapter = document.createElement("div")
            secChapterWrap.appendChild(secChapter)
            secChapter.classList.add("chapterBorder02")
            getSec03Height();
            linkWrapVis();
        })
        window.addEventListener('resize',()=>{
            getSec03Height();
            linkWrapVis();
        })

    }
}
</script>

<style lang="scss">
@import "@/assets/scss/thirdArea.scss";
</style>