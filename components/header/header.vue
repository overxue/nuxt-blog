<template>
  <div class="header">
    <div class="header-container">
      <nuxt-link to="/" class="header-left">
        <span class="header-blank" />
        <img src="https://surmon.me/images/logo.svg" class="header-logo">
        <span class="header-desc">欢喜勇猛，向死而生</span>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<script lang="stylus" scoped>
  .header
    position: fixed
    top: 0
    left: 0
    width: 100%
    height: 63px
    background-color: rgba(255, 255, 255, 0.6)
    z-index: 10
    .header-container
      height: 100%
      width: 1170px
      margin: 0 auto
      .header-left
        display: flex
        position: relative
        align-items: center
        height: 100%
        width: 400px
        padding-left: 5px
        .header-blank
          position: absolute
          top: 0
          left: 0
          width: 60%
          height: 100%
          opacity: 0
          animation: logo-blink 8s ease-in 1s infinite
          &:before
            content: ''
            width: 11rem;
            height: 3rem;
            position: absolute
            top: 15%
            left: 0
            transform: rotate(-45deg)
            background: radial-gradient(white, rgba(255, 255, 255, .2), rgba(255, 255, 255, 0));
        .header-logo
          width: 117.3px
          margin-right: 40px
        .header-desc
          font-family: DINRegular
          color: #0088f5
          font-size: 14px
    @keyframes logo-blink {
      0% {
        opacity: 0;
        transform: translateX(-10%);
      }
      5% { opacity: 1 }
      35% { opacity: 1 }
      39% { opacity: 0 }
      50% { opacity: .8 }
      60% { opacity: .8 }
      65% {
        opacity: .8;
        transform: translateX(100%);
      }
      70% {
        opacity: 0;
        transform: translateX(100%);
      }
      100% {
        opacity: 0;
        transform: translateX(100%);
      }
    }
</script>
