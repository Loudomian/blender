<template>
  <div class="up-example">
    <div class="blog-list-wrapper">
      <div class="blog-item" v-for="(blog, index) in examplesData" :key="index">
        <img class="thumbnail" :src="blog.thumbnail" alt="缩略图">
        <div class="info">
          <h4 class="title">{{ blog.name }}</h4>
          <p class="desc">{{ blog.desc }}</p>
          <a class="btn" target="blank" :href="blog.link">围观</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import examplesData from '../data/examplesData'

export default {
  data () {
    return {
      examplesData
    }
  }
}
</script>


<style lang="stylus" scoped>
.up-example
  .blog-list-wrapper
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    .blog-item
      margin-bottom 4rem
      width 31%
      box-shadow: var(--box-shadow)
      transition: all .5s
      .info
        margin 2.5rem  0 1.5rem
        padding 0 1.5rem
        .title
          margin 0
          max-width 65%
          overflow hidden
          text-overflow ellipsis
          white-space nowrap
        .desc
          margin .6rem 0 1.5rem
          overflow hidden
          text-overflow ellipsis
          white-space nowrap
          font-size 12px
        .btn
          display inline-block
          background-color $accentColor  
          color #ffffff
          border-radius 2px
          padding 2px 5px
          font-size 12px
          text-decoration none 
          cursor pointer
      &:hover
        transform scale(1.05)

@media (max-width: $MQMobile)
  .up-example
    .blog-list-wrapper
      .blog-item
        width 100%
</style>

