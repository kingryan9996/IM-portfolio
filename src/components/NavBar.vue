<template>
  <article class="navbar-wrap" ref="navBarWrap">
    <div class="first-line">
        <h2 class="logo" @click="secNavigator(0)">ISH</h2>
    </div>
    <div class="second-line">
        <ul class="hamburger" ref="hamburgerList">
            <li v-for="(list,index) in hamburger" :key="index" :class="list" @click="secNavigator(index)">{{list}}</li>
            <!-- <li class="title">TITLE</li>
            <li class="about">ABOUT</li>
            <li class="work">WORK</li> -->
        </ul>
    </div>
    <div class="third-line">
        <ul>            
            <li>서울시 관악구</li>
            <li>kingryan9996@gmail.com</li>
            <li class="sns-link">
                <span><svg xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 24 30" width="24px" height="24px" fill="#999999"><path d="M 6 4 C 4.9069372 4 4 4.9069372 4 6 L 4 14.832031 A 1.0001 1.0001 0 0 0 4 15.158203 L 4 19.832031 A 1.0001 1.0001 0 0 0 4 20.158203 L 4 24 C 4 25.093063 4.9069372 26 6 26 L 24 26 C 25.093063 26 26 25.093063 26 24 L 26 20.167969 A 1.0001 1.0001 0 0 0 26 19.841797 L 26 15.167969 A 1.0001 1.0001 0 0 0 26 14.841797 L 26 6 C 26 4.9069372 25.093063 4 24 4 L 6 4 z M 6 11 L 24 11 L 24 14 L 6 14 L 6 11 z M 6 16 L 24 16 L 24 19 L 6 19 L 6 16 z M 6 21 L 24 21 L 24 24 L 6 24 L 6 21 z"/></svg></span>
                <span><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0,0,256,256" width="24px" height="24px" fill-rule="nonzero"><g fill="#999999" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><g transform="scale(10.66667,10.66667)"><path d="M8,3c-2.757,0 -5,2.243 -5,5v8c0,2.757 2.243,5 5,5h8c2.757,0 5,-2.243 5,-5v-8c0,-2.757 -2.243,-5 -5,-5zM8,5h8c1.654,0 3,1.346 3,3v8c0,1.654 -1.346,3 -3,3h-8c-1.654,0 -3,-1.346 -3,-3v-8c0,-1.654 1.346,-3 3,-3zM17,6c-0.55228,0 -1,0.44772 -1,1c0,0.55228 0.44772,1 1,1c0.55228,0 1,-0.44772 1,-1c0,-0.55228 -0.44772,-1 -1,-1zM12,7c-2.757,0 -5,2.243 -5,5c0,2.757 2.243,5 5,5c2.757,0 5,-2.243 5,-5c0,-2.757 -2.243,-5 -5,-5zM12,9c1.654,0 3,1.346 3,3c0,1.654 -1.346,3 -3,3c-1.654,0 -3,-1.346 -3,-3c0,-1.654 1.346,-3 3,-3z"></path></g></g></svg></span>
                <span><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0,0,256,256" width="24px" height="24px" fill-rule="nonzero"><g fill="#999999" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><g transform="scale(10.66667,10.66667)"><path d="M11.666,2.005c-5.046,0.165 -9.292,4.246 -9.641,9.283c-0.369,5.329 3.442,9.832 8.481,10.589v-7.227h-1.614c-0.726,0 -1.314,-0.588 -1.314,-1.314v0c0,-0.726 0.588,-1.314 1.314,-1.314h1.613v-1.749c0,-2.896 1.411,-4.167 3.818,-4.167c0.357,0 0.662,0.008 0.921,0.021c0.636,0.031 1.129,0.561 1.129,1.198v0c0,0.663 -0.537,1.2 -1.2,1.2h-0.442c-1.022,0 -1.379,0.969 -1.379,2.061v1.437h1.87c0.591,0 1.043,0.527 0.953,1.111l-0.108,0.701c-0.073,0.47 -0.477,0.817 -0.953,0.817h-1.762v7.247c4.883,-0.663 8.648,-4.837 8.648,-9.899c0,-5.634 -4.659,-10.179 -10.334,-9.995z"></path></g></g></svg></span>
            </li>
        </ul>
    </div>
  </article>
</template>

<script>

export default {
    mounted() {
        const sectionList = document.querySelectorAll(".second-line > ul > li")
        const firstSec = document.querySelector(".first-area-wrap")
        const thirdSec = document.querySelector(".third-area-wrap")
        const secondSec = document.querySelector(".second-area-wrap")        
        
        // console.log(firstSec.clientHeight,'?????')
        // console.log(firstSec.offsetTop,'?????')
        // console.log(secondSec.clientHeight,'?????')
        // console.log(secondSec.offsetTop,'?????')
        // console.log(thirdSec.clientHeight,'?????')
        // console.log(thirdSec.offsetTop,'?????')

                document.addEventListener('scroll',()=>{
                    console.log(this.$refs.hamburgerList.clientWidth)
                // console.log(window.innerHeight)
                if ( firstSec.offsetTop >= 0 && window.pageYOffset < firstSec.clientHeight -150 ){
                    // sectionList[0].classList.add("active")
                    classRemove(0)
                    // console.log('첫번째섹션')
                    this.$refs.hamburgerList.style["color"] = "#FFF"
                } else if ( ( window.pageYOffset >= firstSec.clientHeight - this.$refs.hamburgerList.clientWidth ) && window.pageYOffset < ( ( firstSec.clientHeight + secondSec.clientHeight ) - this.$refs.hamburgerList.clientWidth ) ){
                    classRemove(1)
                    this.$refs.hamburgerList.style["color"] = "#000"
                } else if ( window.pageYOffset >= ( ( firstSec.clientHeight + secondSec.clientHeight ) - this.$refs.hamburgerList.clientWidth ) && secondSec.clientHeight + thirdSec.clientHeight ){
                    classRemove(2)
                    this.$refs.hamburgerList.style["color"] = "#FFF"
                }
            }
        )


        const classRemove = (num) => {
            sectionList.forEach((e,index)=> {
            if (index!=num ) { e.classList.remove("active")
            } else if ( index==num && e.className != "active" ) {
                e.classList.add("active")
            }
            })
        }


        const getNavBarHeight = () => {
            this.$refs.navBarWrap.style["height"] = `${document.querySelector(".first-area-wrap").clientHeight}px`
        }

        window.addEventListener("load",()=>{
            getNavBarHeight()
            setTimeout(()=>{
            this.$refs.hamburgerList.childNodes[1].classList.add("active")
            },5800)
        })

        window.addEventListener("resize",()=>{
            getNavBarHeight()
        })




       
    },
    data() {
        return {
        hamburger: ["title","about","work"]
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
    width: 230px;
    min-height: 350px;
    color: #FFF;
    .first-line {
        position:fixed;
        top: 5%;
        left: 3%;
        h2::before {
            display: block;
            content: "";
            width: 1.4rem;
            height: 1.4rem;
            border: 1.5px solid #FFF;
            position: absolute;
            top: 0;
            left: 0;
            z-index: -1;            
            transform: translate(-30%,-5%);
        }
        h2 {
            font-size: 2rem;
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
    }
    .second-line {
        .hamburger {
            position: fixed;
            top: 15%;
            right: -3%;
            display: flex;
            justify-content: space-between;
            width: 11vw;
            transform: rotateZ(90deg);
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
    .third-line {
        ul {
            li {
                font-size: 10px;
                text-align: left;
                line-height: 15px;
                opacity: 0.6;
            }
            .sns-link{
                display: flex;
                
                margin: 6% 0 0 -5px;
                span:hover > svg > g{
                    fill: #FFF;
                    transition: 0.2s;
                    opacity: 1;
                }
                span:hover > svg{
                    fill: #FFF;
                    transition: 0.2s;
                    opacity: 1;
                }
            }
        }
    }    
}
</style>