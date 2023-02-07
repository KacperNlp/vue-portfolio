<template>
  <section class="section about-me" id="about-me">
    <base-headline><h1>about me</h1></base-headline>
    <div class="about-me-subheadline">
      <p><span>22 years</span><span>Reszów</span><span>Poland</span></p>
    </div>
    <base-description
      ><p class="about-me-description">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pharetra
        tincidunt diam, ac commodo orci ullamcorper eu. Nulla imperdiet, mi
        lobortis convallis porttitor, magna dui pretium est, a porttitor justo
        turpis et ligula. Nulla interdum dapibus leo, id sagittis risus semper
        quis. Suspendisse venenatis diam id interdum pellentesque. Mauris
        commodo neque finibus odio finibus placerat. Proin feugiat faucibus
        lorem. Cras consectetur, velit ut volutpat cursus, sem metus efficitur
        erat, a blandit magna sem et odio. Phasellus rhoncus lacus in lacus
        laoreet hendrerit. Sed eu faucibus augue. Nullam placerat ornare ipsum,
        sed blandit lacus feugiat a. Orci varius natoque penatibus et magnis dis
        parturient montes, nascetur ridiculus mus. Proin risus lectus, pretium
        eget urna non, faucibus pulvinar dolor. Ut sit amet orci diam. Aenean id
        viverra ipsum. Aenean maximus lacus ac venenatis consequat.
      </p></base-description
    >
  </section>
</template>
<script>
import BaseDescription from "../base/BaseDescription.vue";
import BaseHeadline from "../base/BaseHeadline.vue";

export default {
  name: "SectionAboutMe",
  components: { BaseDescription, BaseHeadline },
};
</script>
<style lang="scss">
.about-me {
  padding-top: 100px;

  &-subheadline {
    margin-top: 20px;
    color: #cd5888;

    span {
      position: relative;
      padding-right: 20px;
      padding-left: 20px;
      font-size: 14px;
      font-style: italic;

      @media (min-width: 1024px) {
        font-size: 16px;
      }

      &:first-child {
        padding-left: 0;
      }

      &::before {
        position: absolute;
        right: 0;
        width: 1px;
        height: 20px;
        content: "";
        background: #e9e8e8;
        transform: rotate(25deg);
      }

      &:last-child::before {
        content: none;
      }
    }
  }

  &-description {
    margin-top: 40px;
  }
}
</style>
