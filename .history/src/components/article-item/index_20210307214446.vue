<!-- 文章列表项 -->
<template>
  <van-cell
  class="artic-item"
  >
  <div slot="title" class="title">{{article.title}}</div>
  <div slot="label">
  <div v-if="article.cover.type===3" class="cover-wrap">
    <div class="cover-item" v-for="(img,index) in article.cover.images">
     <van-image
       width="100"
       height="100"
       :src="article.cover.images[0]"
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

<style scoped lang="less"></style>
