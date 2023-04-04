<template>
  <article class="third-area-wrap">
    <div class="third-left">
        <div class="section-02">
            <div class="section-number">02</div>
            <div class="section-title">
                <span>PROJECT</span>
            </div>
        </div>
        <div>
            <div class="work-description" v-html="workDescription"/>
        </div>
    </div>
    <div class="third-right">
        <ul class="third-right-items">
            <li><img src="https://i.pinimg.com/564x/c1/d2/eb/c1d2ebf48a6367de7e7453f5befd3e2f.jpg"></li>
            <li><img src="https://i.pinimg.com/564x/56/15/dd/5615dde0afe82cd720b1a7d85d233d9d.jpg"></li>
            <li><img src="https://i.namu.wiki/i/czsnXEycUIHHMNiwukY5hamUqk3ry6J7iB1EiB0J-3VW2WjmuAJzlkipi0clu8kSGxzCX-T1UsBmotSbhzMC4I-9wrJcmNX78OzV6tQYWV30f-kYN8ArBxLEtUuQgR5vLuLbIn3b4To_9zlKpa5F0A.webp"></li>
        </ul>
    </div>
  </article>
</template>

<script>
export default {
    data() {
        return {
            workDescription:""
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
                    this.workDescription = "프로젝트 공간"
                } else if ( window.pageYOffset > ( thirdSec.offsetTop + workList[0].offsetTop ) && ( window.pageYOffset < thirdSec.offsetTop + workList[1].offsetTop ) ){
                    this.workDescription = "첫번째 작품"
                } else if ( window.pageYOffset > ( thirdSec.offsetTop + workList[1].offsetTop ) && ( window.pageYOffset < thirdSec.offsetTop + workList[2].offsetTop ) ){
                    this.workDescription = "두번째 작품"
                } else if ( window.pageYOffset > ( thirdSec.offsetTop + workList[2].offsetTop ) ){
                    this.workDescription = "세번째 작품"
                }
            }
        )

        const getSec03Height = () => {

            const leftSide02Div = document.querySelector(".third-left")
            const chapterBorder = document.querySelector(".chapterBorder02")

            leftSide02Div.style = `
            height: ${workList[0].clientHeight}px;
            padding-top: ${workList[0].clientHeight / 5}px;
            margin-bottom: ${workList[0].clientHeight / 2}px`;

            // console.log(leftSide02Div)
            chapterBorder.style = `
            position: absolute;
            border-top: 1px solid #FFF;
            width: ${leftSide02Div.clientHeight / 1.6}px;
            top: 50%;
            left: 110%;
            transform: translateY(-50%);`;
        }

        window.addEventListener("load",()=>{
            const secChapterWrap = document.querySelector(".section-02 > .section-title ")
            const secChapter = document.createElement("div")
            secChapterWrap.appendChild(secChapter)
            secChapter.classList.add("chapterBorder02")

            getSec03Height();
        })
        window.addEventListener('resize',()=>{
            getSec03Height();
        })

    }
}
</script>

<style lang="scss">
.third-area-wrap {
    padding: 20% 220px 10%;
    position: relative;
    background-color: #000;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    color: #FFF;    
    .third-left {
        width: 40%;
        padding-left: 10%;
        position:sticky;
        top:10%;
        .section-02 {
            height: 100%;
            position: absolute;
            top: 18%;
            left: -10%;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-content: center;
            .section-number {
                font-size: 4vw;
                font-weight: 700;
                position: static;
                background-color: #000;
                z-index: 1;
            }
            .section-title {
                position:relative;
                transform: rotateZ(270deg);
                font-size: 1.6vw;
                font-weight: 400;
                }
            }
            .work-description {
            width: 100%;
            font-size: 3vw;
            display: block;            
            text-align: left;
            }               
        }
    .third-right {
        width: 60%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        .third-right-items {
            width: 100%;
            transform: translateY(-5%);
            li {   
                position: sticky;
                top:30%;
                img {
                    width: 100%;
                    --p:(width * 3)px;
                    height: --p;
                    box-shadow: 0 0 30px rgba(0,0,0,0.4);
                }
            }
        }
    }
}
</style>