<template>
  <div class="recommend">
    <div class="recom-item" v-for="(item, key) in recommends" :key="key">
      <a :href="item.link">
        <img :src="item.image" alt="" />
        <div>{{ item.title }}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "RecommendView",
  props: {
    recommends: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style scoped>
.recommend {
  display: flex;
  width: 100%;
  text-align: center;
  font-size: 12px;
  padding: 10px 0 20px;
  border-bottom: 10px solid #eee;
}
.recom-item {
  flex: 1;
}
.recom-item img {
  width: 70px;
  height: 70px;
  margin-bottom: 10px;
}
</style>
