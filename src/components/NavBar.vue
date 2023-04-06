<template>
  <article class="navbar-wrap" ref="navBarWrap">
    <div class="first-line">
        <h2 ref="navLogo" class="blueW" @click="secNavigator(0)">ISH</h2>
    </div>
        <ul class="hamburger" ref="hamburgerList">
            <li v-for="(list,index) in hamburger" :key="index" :class="list" @click="secNavigator(index)">{{list}}</li>
            <!-- <li class="title">TITLE</li>
            <li class="about">ABOUT</li>
            <li class="work">WORK</li> -->
        </ul>
        <div class="btn-goTop" @click="scTopScrollFn()">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 12 24">
                <path d="M7.07095 12L3.24995 8.17903C2.83595 7.76503 2.83595 7.09303 3.24995 6.67903C3.66395 6.26503 4.33595 6.26503 4.74995 6.67903L9.36395 11.293C9.75495 11.684 9.75495 12.317 9.36395 12.707L4.74995 17.321C4.33595 17.735 3.66395 17.735 3.24995 17.321C2.83595 16.907 2.83595 16.235 3.24995 15.821L7.07095 12Z"></path>
            </svg>
            <svg class="arr02" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 12 24">
                <path d="M7.07095 12L3.24995 8.17903C2.83595 7.76503 2.83595 7.09303 3.24995 6.67903C3.66395 6.26503 4.33595 6.26503 4.74995 6.67903L9.36395 11.293C9.75495 11.684 9.75495 12.317 9.36395 12.707L4.74995 17.321C4.33595 17.735 3.66395 17.735 3.24995 17.321C2.83595 16.907 2.83595 16.235 3.24995 15.821L7.07095 12Z"></path>
            </svg>
        </div>
  </article>
</template>

<script>
export default {
    mounted() {
        const sectionList = document.querySelectorAll(".hamburger > li")
        const firstSec = document.querySelector(".first-area-wrap")
        const thirdSec = document.querySelector(".third-area-wrap")
        const secondSec = document.querySelector(".second-area-wrap")
        const logoEl = this.$refs.navLogo
        console.log(logoEl,'???')
        
        // console.log(firstSec.clientHeight,'?????')
        // console.log(firstSec.offsetTop,'?????')
        // console.log(secondSec.clientHeight,'?????')
        // console.log(secondSec.offsetTop,'?????')
        // console.log(thirdSec.clientHeight,'?????')
        // console.log(thirdSec.offsetTop,'?????')

                document.addEventListener('scroll',()=>{
                    logoClassFn();
                    let hamVisTunning = ( this.$refs.hamburgerList.clientWidth * 0.80 )
                if ( firstSec.offsetTop >= 0 && window.pageYOffset < firstSec.clientHeight - hamVisTunning ){
                    classRemove(0)
                    this.$refs.hamburgerList.style["color"] = "#FFF"
                } else if ( ( window.pageYOffset >= firstSec.clientHeight - hamVisTunning ) && window.pageYOffset < ( ( firstSec.clientHeight + secondSec.clientHeight ) - hamVisTunning ) ){
                    classRemove(1)
                    this.$refs.hamburgerList.style["color"] = "#000"
                } else if ( window.pageYOffset >= ( ( firstSec.clientHeight + secondSec.clientHeight ) - hamVisTunning ) && secondSec.clientHeight + thirdSec.clientHeight ){
                    classRemove(2)
                    this.$refs.hamburgerList.style["color"] = "#FFF"
                }
            }
        )

        const logoClassFn = () => {
            console.log(( firstSec.clientHeight / 18 ))
            let logoVisTunning = ( firstSec.clientHeight / 18 )
            if ( firstSec.offsetTop >= 0 && window.pageYOffset < firstSec.clientHeight - logoVisTunning && logoEl.className != "blueW" ){
                logoEl.className = "blueW"
            } else if ( ( window.pageYOffset >= firstSec.clientHeight - logoVisTunning ) && window.pageYOffset < ( firstSec.clientHeight + secondSec.clientHeight - logoVisTunning ) && logoEl.className != "blackW" ){
                logoEl.className = "blackW"
            } else if ( window.pageYOffset >= ( firstSec.clientHeight + secondSec.clientHeight -logoVisTunning ) && secondSec.clientHeight + thirdSec.clientHeight && logoEl.className != "Wblack" ){
                logoEl.className = "Wblack"
            }
        }


        const classRemove = (num) => {
            sectionList.forEach((e,index)=> {
                    if (index!=num ) { e.classList.remove("active")
                    } else if ( index==num && e.className != "active" ) {
                        e.classList.add("active")
                    }
                }
            )
        }


        const getNavBarHeight = () => {
            this.$refs.navBarWrap.style["height"] = `${document.querySelector(".first-area-wrap").clientHeight}px`
        }

        window.addEventListener("load",()=>{
            // getNavBarHeight()
            setTimeout(()=>{
            this.$refs.hamburgerList.childNodes[1].classList.add("active")
            },5800)
        })

        window.addEventListener("resize",()=>{
            // getNavBarHeight()
        })
    },
    data() {
        return {
        hamburger: ["main","about","work"]
        }
    },
    methods: {
        
         secNavigator: function (index) {

            const allArticle = document.querySelectorAll("article")
            const secThree = [];
            allArticle.forEach((obj,index)=>{
                if(index == 1 || index == 3 || index == 4) {
                    secThree.push(obj)
                }
            })
            window.scrollTo({
                top: secThree[index].offsetTop,
                left: 0,
                behavior: 'smooth'
            });
        },

        scTopScrollFn: function () {
            window.scrollTo({
                top: 0,
                left: 0,
                behavior: 'smooth'
            });
        }


    },
}
</script>

<style lang="scss">
.navbar-wrap{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    position: fixed;
    z-index: 10;
    top: 0;
    left: 0;    
    .first-line {
        position:fixed;
        top: 5%;
        left: 3%;
        h2::before {
            display: block;
            content: "";
            width: 1.4rem;
            height: 1.4rem;            
            position: absolute;
            top: 0;
            left: 0;
            z-index: -1;
            transform: translate(-30%,-5%);
        }
        h2 {
            font-size: 2rem;            
        }
        .blueW::before {
            border: 1.5px solid #FFF;
        }
        .blueW {
            color: #FFF;
            &:hover{
                cursor: pointer;
                color: #0338d6;
                -webkit-text-stroke: .5px #FFF;
            }
            &:hover::before{
                background-color: rgba(255,255,255,0.95);
                border-color: #0338d6;
            }
        }
        .blackW::before {
            border: 1.5px solid #000;
        }
        .blackW {
            color: #000;
            &:hover{
                cursor: pointer;
                color: #FFF;
                -webkit-text-stroke: 1.5px #000;
            }
            &:hover::before{
                background-color: rgba( 0,0,0,0.95);
                border-color: #FFF;
            }
        }
        .Wblack::before {
            border: 1.5px solid #FFF;
        }
        .Wblack {
            color: #FFF;
            &:hover{
                cursor: pointer;
                color: #000;
                -webkit-text-stroke: 0.5px #FFF;
            }
            &:hover::before{
                background-color: rgba( 255,255,255,0.95);
                border-color: #FFF;
            }
        }
    }
        .hamburger::before {
            display: block;
            content: "";
            position: fixed;
            width: 11vw;
            min-width: 103px;
            border-bottom: 1px solid;
            bottom: 0;
            left: 150%;
            // transform: translateX(150%);
            animation-name: hamBeforeArrow;
            animation-duration: 10s;
            animation-delay: 6.2s;
            animation-direction: alternate;
            animation-iteration-count: infinite;
        }
        .hamburger::after {
            display: block;
            content: "";
            position: fixed;
            width: 1.5vw;
            min-width: 15px;
            border-bottom: 1px solid;
            bottom: 0.5vw;
            left: 238%;
            //반응형 500기준 245%로 변경요망
            transform: rotateZ(45deg);
            animation-name: hamAfterArrow;
            animation-duration: 10s;
            animation-delay: 6.2s;
            animation-direction: alternate;
            animation-iteration-count: infinite;
        }
        @keyframes hamBeforeArrow {
            0% {

            }
            50% {
                transform: translateX(50px);
            }
            100% {

            }
        }
        @keyframes hamAfterArrow {
            0% {

            }
            50% {
                transform: translateX(50px) rotateZ(45deg);
            }
            100% {

            }
        }
        .hamburger {
            position: fixed;
            top: 20%;
            right: -3%;
            display: flex;
            justify-content: space-between;
            width: 11vw;
            min-width: 103px;
            transform: rotateZ(90deg);
            color:#FFF;
            li {
                font-size: .8vw;
                text-align: left;
                text-transform: uppercase;
                opacity: 0.5;
                // mix-blend-mode: difference;                
                font-weight: 700;
                &.active{
                    // color:#4BDFFA;
                    animation-name: hamListScale;
                    animation-duration: 500ms;
                    animation-fill-mode: forwards;
                    mix-blend-mode: difference;
                }
                @keyframes hamListScale {
                    to {
                        opacity: 1;
                        text-decoration: line-through 1.5px;
                    }
                }
                &:hover{
                    cursor: pointer;
                }
            }
            li:nth-child(2) {
                margin: 0;
            }           
        }
        .btn-goTop {
            position: fixed;
            right: 1%;
            bottom: 4.5%;
            width: 1.5vw;
            height: 1.5vw;
            cursor: pointer;
            animation-name: goTopAni;
            animation-duration: 5s;
            animation-iteration-count: infinite;
            animation-direction: alternate;
            @keyframes goTopAni {
                // 0% {}
                25% {
                    transform: scale3d(0.9,1.15,1);
                }
                50% {
                    transform: scale3d(1,1,1) translateY(-20%);
                }
                70% {
                    transform: scale3d(0.9,1.15,1);
                }
                // 100% {}
            }
            &:hover {
                animation-name: goTopAniStop;
            }
            &:hover svg {
                // fill: skyblue;
                stroke: #000;
                
            }
            &:hover .arr02 {
                transition: 0.7s;
                transform: translateY(20%) rotateZ(-90deg);
            }
            svg {
                position: absolute;
                top: 0;
                left: 0;
                transform: rotateZ(-90deg);
                fill: skyblue;
                stroke-width:.3;
                // path {
                //     stroke-width:.5;
                //     // stroke: #FFF;
                // }
            }
        }          
}
</style>