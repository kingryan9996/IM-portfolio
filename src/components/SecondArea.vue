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

}
</script>

<style lang="scss">
.second-area-wrap {
    margin: 10vh 0 20vh;
    display: flex;
    height: 100vh;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    .second-left {
        width: 40%;
        .left-wrap {
            position: relative;
            height: 3vw;
            h2 {
            position: absolute;
            top: 0;
            left: 0;
            font-size: 3vw;
            display: block;
            width: 1000px;
            text-align: left;
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
            li {                
                img {
                    width: 100%;
                    height: 300px;
                }
            }
        }
    }
}
</style>