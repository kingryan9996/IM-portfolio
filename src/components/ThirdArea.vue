<template>
  <article class="third-area-wrap">
    <div class="third-left">
        <div class="left-wrap">
            <h2>WORK ABOUT SKILL</h2>
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
    mounted() {

        const workList = document.querySelectorAll(".third-right-items > li")

        document.querySelector(".left-wrap").style["padding-bottom"] = `${ (workList[1].clientHeight / 100 ) * 60 }px`;

        console.log(workList)

        console.log(document.querySelector(".left-wrap > h2"))


        document.addEventListener('scroll',()=>{
                // console.log(window.innerHeight)
                if ( window.pageYOffset > workList[0].clientHeight ){
                    // sectionList[0].classList.add("active")
                    console.log("첫번째 작품")
                } 
                // else if ( window.pageYOffset >= firstSec.clientHeight && window.pageYOffset < ( firstSec.clientHeight + secondSec.clientHeight ) ){
                //     classRemove(1)
                // } else if ( window.pageYOffset >=( firstSec.clientHeight + secondSec.clientHeight ) && secondSec.clientHeight + thirdSec.clientHeight ){
                //     classRemove(2)
                // }
            }
        )

        // const classRemove = (num) => {
        //     sectionList.forEach((e,index)=> {
        //     if (index!=num ) { e.classList.remove("active")
        //     } else if ( index==num && e.className != "active" ) {
        //         e.classList.add("active")
        //     }
        //     })
        // }
        




    }
}
</script>

<style lang="scss">
.third-area-wrap {
    margin-bottom: 25%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    
    .third-left {
        width: 40%;
        .left-wrap {
            position: sticky;
            top:50%;
            z-index: 5;            
            h2 {
            width: 120%;
            position: absolute;
            left: 0;
            font-size: 3vw;
            display: block;            
            text-align: left;
            transform: translateY(-75%);
            }
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
                    height: 530px;
                    box-shadow: 0 0 30px rgba(0,0,0,0.4);
                }
            }
        }
    }
}
</style>