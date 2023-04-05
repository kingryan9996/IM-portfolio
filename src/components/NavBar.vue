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
            border-bottom: 1px solid;
            bottom: 0;
            left: 150%;
            // transform: translateX(150%);
            animation-name: hamBeforeArrow;
            animation-duration: 5s;
            animation-direction: alternate;
            animation-iteration-count: infinite;
        }
        .hamburger::after {
            display: block;
            content: "";
            position: fixed;
            width: 1.5vw;
            border-bottom: 1px solid;
            bottom: 0.5vw;
            left: 238%;
            transform: rotateZ(45deg);
            animation-name: hamAfterArrow;
            animation-duration: 5s;
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
                        text-decoration: line-through;
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
    
}
</style>