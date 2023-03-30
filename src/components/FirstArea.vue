<template>
<article class="first-area-wrap">
  <h1>
    <span>F</span>
    <span>r</span>
    <span>o</span>
    <span>n</span>
    <span>t</span>
    <p>
      Hi,<br/>
      I'M 승환,<br/>
      프론트엔드로 취업을 준비중인

    </p>
  </h1>
    <span class="And">&</span>
  </article>
</template>

<script>
export default {

}

</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Nanum+Myeongjo&display=swap');

.first-area-wrap {
  height: 100vh;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-content: center;
  h1::before{
    content: "I'M 승환";
    display: block;
    position: absolute;
    top: 7%;
    left: 26%;
    font-size: 30px;
  }
  h1::before:nth-child(5) {
    color: red;
  }
  h1{
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
    }
  }
    .And{
      line-height: 400px;
      font-size: 450px;
      font-weight: 100;
      font-family: 'Nanum Myeongjo', serif;
    }
}

</style>