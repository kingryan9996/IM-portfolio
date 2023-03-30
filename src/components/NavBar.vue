<template>
  <article class="navbar-wrap">
    <div class="first-line"><h2>ISH</h2></div>
    <div class="second-line">
        <ul>
            <li>WORK</li>
            <li>ABOUT</li>
            <li>SKILL</li>
        </ul>
    </div>
    <div class="third-line">
        <ul>
            <li>010-9996-5765</li>
            <li>서울시 관악구</li>
            <li>kingryan9996@gmail.com</li>
            <li>
                <span>인스타그램</span>
                <span>페이스북</span>
                <span>카카오톡</span>
            </li>
        </ul>
    </div>
  </article>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.navbar-wrap{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    position: fixed;
    top: 0;
    left: 0;
    width: 230px;
    height: 100vh;
    border-right: 1px solid #F53D44;
    .first-line {
        position:relative;
        h2::before {
            display: block;
            content: "";
            width: 1.4rem;
            height: 1.4rem;
            background-color: #F53D44;
            position: absolute;
            top: 0;
            left: 0;
            z-index: -1;            
            transform: translate(-30%,-5%);
        }
        h2 {
            font-size: 2rem;
        }
    }
    .second-line {

    }
    .third-line {

    }
}
</style>