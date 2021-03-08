<!-- 文章列表项 -->
<template>
  <van-cell
  class="artic-item"
  >
  <div slot="title" class="title van-multi-ellipsis--l2">{{article.title}}</div>
  <div slot="label">
  <div v-if="article.cover.type===3" class="cover-wrap">
    <div
    class="cover-item"
    v-for="(img,index) in article.cover.images"
    :key="index"
    >
    </div>
  </div>
  <div class="lable-info-wrap">
    <span>{{article.aut_name}}</span>
    <span>{{article.collect_count}}评论</span>
    <span>{{article.pubdate}}</span>
  </div>

  </div>
  <van-image
     v-if="article.cover.type === 1"
     slot="default"
     class="right-cover"
     fit="cover"
     :src="article.cover.images[0]"
    />
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
    padding-left: 25px;
  }
  .right-cover {
    width: 232px;
    height: 146px;
  }
}
</style>
