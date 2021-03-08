<!-- 文章列表项 -->
<template>
  <van-cell
  class="artic-item"
  >
  <div slot="title" class="title">{{article.title}}</div>
  <div slot="label">
  <span>{{article.label}}</span>
  <span>{{article.label}}</span>
  <span>{{article.label}}</span>
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
