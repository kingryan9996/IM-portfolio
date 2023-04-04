<template>
<article class="first-area-wrap">  
  <h1>
    <div class="svg-path">
      <div class="svg-text-wrap">
        <div class="svg-portfolio">
        <svg class="text-svg p">
          <text x="0" y="120" >
            P
          </text>
        </svg>
        <svg class="text-svg o">
          <text x="0" y="120" >
            o
          </text>
        </svg>
        <svg class="text-svg r">
          <text x="0" y="120" >
            r
          </text>
        </svg>
        <svg class="text-svg t">
          <text x="0" y="120" >
            t
          </text>
        </svg>
        <svg class="text-svg f">
          <text x="0" y="120" >
            f
          </text>
        </svg>
        <svg class="text-svg o">
          <text x="0" y="120" >
            o
          </text>
        </svg>
        <svg class="text-svg l">
          <text x="0" y="120" >
            l
          </text>
        </svg>
        <svg class="text-svg i">
          <text x="0" y="120" >
            i
          </text>
        </svg>
        <svg class="text-svg o">
          <text x="0" y="120" >
            o
          </text>
        </svg>
        </div>
        <div class="svg-Front">
          <svg class="text-svg F">
            <text x="0" y="130" >
              F
            </text>
          </svg>
          <svg class="text-svg r">
            <text x="0" y="130" >
              r
            </text>
          </svg>
          <svg class="text-svg o">
            <text x="0" y="130" >
              o
            </text>
          </svg>
          <svg class="text-svg n">
            <text x="0" y="130" >
              n
            </text>
          </svg>
          <svg class="text-svg t">
            <text x="0" y="130">
              t
            </text>
          </svg>          
        </div>
        </div>
        <div class="svg-And">
          <svg class="text-svg And">
            <text x="0" y="300">
              &
            </text>
          </svg>
        </div>
      </div>
  </h1>
    <!-- <span class="And">&</span> -->
    <MyCanvas/>
  </article>
</template>

<script>
import MyCanvas from './MyCanvas.vue';
export default {
   components: {MyCanvas},
  
   mounted() {
    let paths = document.querySelectorAll(".first-area-wrap .svg-portfolio text");
    let texts = document.querySelectorAll('text')

    let startTime = new Date();    

    if (paths.length > 0) {
    setTextAnimation(0.15,2.8,2,'linear','#FFF',true)
  }

  function setTextAnimation(delay, duration, strokeWidth, timingFunction, strokeColor) {
    // if(paths.length == 0){return setTextAnimation(0.15,2.8,2,'linear','#ffffff',true)}
    // let mode=repeat?'infinite':'forwards'
    let mode='forwards'
    // console.log(texts,'??')
              for (let i = 0; i < texts.length; i++) {
                  const text = texts[i];
                  const Textlength = Math.floor(text.textLength.baseVal.value);
                  // console.log(Math.floor(text.textLength.baseVal.value))
                  text.style["stroke-dashoffset"] = `${Textlength}px`;
                  text.style["stroke-dasharray"] = `${Textlength}px`;
                  text.style["stroke-width"] = `${strokeWidth}px`;
                  text.style["stroke"] = `${strokeColor}`;
                  text.style["animation"] = `${duration}s svg-text-anim ${mode} ${timingFunction}`;
                  text.style["animation-delay"] = `${i * delay}s`;
              }
          }


    window.addEventListener('load',()=>{
      const textSvg = document.querySelectorAll(".svg-text-wrap svg")
      const AndSvgEl = document.querySelector(".svg-And > .text-svg")


      AndSvgEl.addEventListener('mouseover',(e)=>{

        let endTime = new Date();
        if (endTime - startTime > 5500)
            if (! e.target.parentElement.classList.contains("active3d")) {
              e.target.parentElement.classList.add("active3d")              
                setTimeout(()=>{
                  e.target.parentElement.classList.remove("active3d")
                },1000)
              }
          }
        )

      textSvg.forEach((item,index) => {        
        textSvg[index].addEventListener('mouseover',(e)=>{

          let endTime = new Date();
          if (endTime - startTime > 5500)
            if (! e.target.parentElement.classList.contains("active3d")) {
              e.target.parentElement.classList.add("active3d")
              if (e.target.style.fill == ""){
                e.target.style.fill = "#FFF"
                setTimeout( () => {
                e.target.style.fill = ""
              },1000)
              }

              setTimeout( () => {
                e.target.parentElement.classList.remove("active3d")
              },1000)
            }          
        })
      })









    })
   }
  }
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Do+Hyeon&family=Inter:wght@300;400;700&display=swap');


.first-area-wrap {
  padding: 7% 180px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-content: center;
  background-color: #0338d6;
  color: #FFF;
  position: relative;
  h1::before{
    content: "I";
    display: block;
    position: absolute;
    top: 32.5%;
    left: 13.8%;
    font-size: 40px;
    color: #4BDFFA;
    opacity: 0;
    animation-name: h1OPacity;
    animation-duration: 5.8s;
    animation-fill-mode: forwards;
  }
  h1::after{
    content: "'M 승환";
    display: block;
    position: absolute;
    top: 31.5%;
    left: 15%;
    font-size: 40px;
    opacity: 0;
    animation-name: h1OPacity;
    animation-duration: 5.8s;
    animation-fill-mode: forwards;
  }
  @keyframes h1OPacity
   {
    95% {
      opacity: 0;
    }
    96% {
      opacity: 0.25;
    }
    97% {
      opacity: 0.5;
    }
    98% {
      opacity: 0.75;
    }
    100% {
      opacity: 1;
    }    
  }
  h1{
    margin-top: 10%;
    scale: 1.3;
    position: relative;    
    span{
      text-align:left;
      vertical-align: text-top;
      font-size: 200px;
    }
    p {
      padding-left:3% ;
      text-align: left;
      font-size: 30px;
      color: #999999;
      color: red;
    }
    .svg-path {
      display: flex;
      .svg-text-wrap {
        width: 700px;
        .svg-portfolio {
          text-align: left;
          font-size: 140px;
          height: 140px;
        .text-svg {
          width: 80px;
          height: 140px;
          font-weight: 700;
          &.active3d {
          animation-name: svg-hover-action;
          animation-duration: 750ms;
          animation-iteration-count: 1;
          }
            
            @keyframes svg-hover-action {
              0%{
                transform:  scale3d(1,1,1);
              }
              30%{
                transform:  scale3d(1.1,0.75,1);
              }
              40%{
                transform:  scale3d(0.75,1.25,1);
              }
              50%{
                transform:  scale3d(1.075,0.85,1);
              }
              65%{
                transform:  scale3d(0.95,1.05,1);
              }
              75%{
                transform:  scale3d(1.025,0.95,1);
              }
              100%{
                transform:  scale3d(1,1,1);
              }
            }
          text {
            fill: none;
            opacity: 0;
          }
        }
        .p {
          width: 88px;
        }
        .o {
          width: 82px;
        }
        .r {
          width: 58px;
        }
        .t {
          width: 53px;
        }
        .f {
          width: 54px;
        }
        .l, .i {
          width: 35px;
        }
      }
      .svg-Front {
        text-align: right;
        font-size: 160px;
        .text-svg {
          width: 80px;
          height: 150px;
          font-weight: 700;
          &.active3d {
          animation-name: svg-hover-action;
          animation-duration: 750ms;
          animation-iteration-count: 1;
          }
            
            @keyframes svg-hover-action {
              0%{
                transform:  scale3d(1,1,1);
              }
              30%{
                transform:  scale3d(1.1,0.75,1);
              }
              40%{
                transform:  scale3d(0.75,1.25,1);
              }
              50%{
                transform:  scale3d(1.075,0.85,1);
              }
              65%{
                transform:  scale3d(0.95,1.05,1);
              }
              75%{
                transform:  scale3d(1.025,0.95,1);
              }
              100%{
                transform:  scale3d(1,1,1);
              }
            }
          text {
            fill: #FFF;
            opacity: 0;
          }
        }
        .F {
          width: 95px;
        }
        .r {
          width: 65px;
        }
        .o {
          width: 95px;
        }
        .n {
          width: 95px;
        }
        .t {
          width: 60px;
        }
        .And {
          width: 35px;
        }
      }
      }
      .svg-And {
        font-size: 400px;
        .text-svg {
          width: 280px;
          height: 400px;
          font-weight: 300;
          &.active3d {
          animation-name: svg-hover-action;
          animation-duration: 750ms;
          animation-iteration-count: 1;
          }
            
            @keyframes svg-hover-action {
              0%{
                transform:  scale3d(1,1,1);
              }
              30%{
                transform:  scale3d(1.1,0.75,1);
              }
              40%{
                transform:  scale3d(0.75,1.25,1);
              }
              50%{
                transform:  scale3d(1.075,0.85,1);
              }
              65%{
                transform:  scale3d(0.95,1.05,1);
              }
              75%{
                transform:  scale3d(1.025,0.95,1);
              }
              100%{
                transform:  scale3d(1,1,1);
              }
            }
          text {
            fill: #FFF;
            opacity: 0;
          }
        }
      }     
    }
      @keyframes svg-text-anim {
        0% {
          fill: transparent;
        }
        20% {
          opacity: 0.2;
          }
        40% {
          stroke-dashoffset: 0;          
          opacity: 0.4;
        }
        60% {
          stroke-dashoffset: 0;
          stroke-dasharray: 20;
          opacity: 0.6;
        }
        80% {
          opacity: 0.8;
        }
        100% {
          stroke-dashoffset: 0;
          stroke-dasharray: 0;
          opacity: 1;

        }        
      }

  }    
}

</style>