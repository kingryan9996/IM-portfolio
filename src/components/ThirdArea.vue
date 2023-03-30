<template>
  <article class="third-area-wrap">
    <div class="third-left">
        <figure>
            <img src="@/assets/img/profile.jpg">
            <figcaption>I'M 승환 About Me</figcaption>
        </figure>
    </div>
    <div class="third-right">
        <h3>ABOUT</h3>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Sit, labore. Voluptate commodi aliquid soluta nihil eum maxime sed. Animi quaerat ad officia, sed impedit consectetur minus fugiat similique qui non.
        Sint, voluptate. Asperiores beatae reprehenderit laborum perspiciatis nostrum laudantium possimus veritatis consectetur consequatur. Culpa iste, fugiat hic a accusantium magni eos voluptatibus nisi vitae pariatur magnam. Velit dolorum odit culpa!
        Natus corrupti quos asperiores. Itaque consequatur facilis provident impedit ea optio voluptatem debitis perspiciatis earum non quis natus culpa voluptates, perferendis odio inventore neque quidem maiores quo quasi nemo. Laborum!
        Beatae ex, ullam ipsum odit iure aut. Aut similique eaque pariatur itaque laudantium nam velit! Aperiam omnis veritatis eaque perferendis officiis adipisci, fuga atque voluptatum nemo, recusandae culpa labore sit?
        Quod, non excepturi recusandae reiciendis beatae aspernatur impedit quis, est ipsa inventore natus culpa accusantium totam. Totam necessitatibus assumenda, magnam placeat accusantium exercitationem deleniti, laudantium perspiciatis rerum tempore culpa vero!</p>
        <h3>SKILL</h3>

    </div>
  </article>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.third-area-wrap {
    height: 100vh;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    .third-left {
        width: 40%;
        position:sticky;
        top:0;
        figure {
            img {
                width: 100%;
            }
        }
    }
    .third-right {
        width: 60%;
    }
}

</style>