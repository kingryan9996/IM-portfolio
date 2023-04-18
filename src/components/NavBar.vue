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
            },3500)
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
@import "@/assets/scss/navbar.scss";
</style>