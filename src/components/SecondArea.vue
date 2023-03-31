<template>
  <article class="second-area-wrap">
    <div class="second-left">
        <div class="left-wrap">
            <h2>WORK ABOUT SKILL</h2>
        </div>
    </div>
    <div class="second-right">
        <ul class="second-right-items">
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
        const h2Padding = ( document.querySelectorAll(".second-right-items > li")[0].clientHeight / 100 ) * 68.5
        document.querySelector(".left-wrap").style["padding-bottom"] = `${h2Padding}px`;
        console.log(h2Padding)
        console.log(document.querySelector(".left-wrap > h2"))

    }
}
</script>

<style lang="scss">
.second-area-wrap {
    margin-bottom: 25%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    
    .second-left {
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
    .second-right {
        width: 60%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        .second-right-items {
            width: 100%;
            transform: translateY(-5%);
            li {   
                position: sticky;
                top:30%;
                img {
                    width: 100%;
                    box-shadow: 0 0 30px rgba(0,0,0,0.4);
                }
            }
        }
    }
}
</style>