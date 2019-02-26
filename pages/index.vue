<template>
  <div class="home">
    <div class="content">
      <div class="avatar">
        <img width="120" height="120" src="https://pigjian.com/images/default_avatar.png" class="avatar-item">
      </div>
      <h1 class="description">
        Nothing is impossible.
      </h1>
      <ul class="tab">
        <li class="tab-item">
          <nuxt-link class="tab-link" to="/blog">
            博文
          </nuxt-link>
        </li>
        <li class="tab-item">
          <a class="tab-link" href="https://weibo.com/3090183841/profile?topnav=1&wvr=6&is_all=1" target="_blank">微博</a>
        </li>
        <li class="tab-item">
          <a class="tab-link" href="https://github.com/overxue" target="_blank">GitHub</a>
        </li>
        <li class="tab-item">
          <nuxt-link class="tab-link" to="/me">
            关于我
          </nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="stylus" scoped>
  .home
    position: relative
    height: 100%
    width: 100%
    .content
      position :absolute
      top: 0
      left: 0
      width: 100%
      height: 100%
      display: flex
      flex-direction: column
      align-items: center
      justify-content: center
      z-index: 3
      text-align: center
      .avatar
        margin-bottom: 20px
        img
          overflow: hidden;
          border-radius: 50%;
          box-shadow: rgba(255, 255, 255, 0.1) 0 0 0 5px, rgba(0, 0, 0, 0.1) 0 0 5px 4px
          transition: transform .4s ease-out
        img:hover
          transform: rotate(360deg)
      .description
        margin-bottom: 20px
        font-weight: bold
        color: #6289ad
        font-size: 24px
      .tab
        .tab-item
          height: 40px
          line-height: 40px
          text-align: center
          list-style: none
          .tab-link
            padding: 10px
            color: #9caebf
            font-size: 14px
            font-weight: 600
          a:hover
            color: #6289ad
            font-weight: 700
</style>
