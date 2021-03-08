<!-- 文章列表项 -->
<template>
  <van-cell
  class="artic-item"
  >
  <div slot="title" class="title">{{article.title}}</div>
  <div slot="label">
  <div v-if="article.cover.type===3" class="cover-wrap">
    <div
    class="cover-item"
    v-for="(img,index) in article.cover.images"
    :key="index"
    >
     <van-image
     v-if="article.cover.type===1"
     class="right-cover"
     slot="default"
       width="100"
       height="100"
       :src="img"
    />
    </div>
  </div>
  <span>{{article.aut_name}}</span>
  <span>{{article.collect_count}}评论</span>
  <span>{{article.pubdate}}</span>
  </div>

  </van-cell>
</template>

<script>
export default {
  name: 'ArticleItem',
  components: {},
  props: {
    article: {
      type: Object,
      required: true
    }
  },
  data () {
    return {}
  },
  computed: {},
  watch: {},
  created () {},
  mounted () {},
  methods: {}
}
</script>

<style scoped lang="less">
.artic-item {
  .title {
     font-size: 32px;
     color: #3a3a3a;
  }
  .van-cell__value {
    flex: unset;
    width: 232px;
    height: 146px;
  }
  .right-cover {
        width: 232px;
    height: 146px;
  }
}
</style>
