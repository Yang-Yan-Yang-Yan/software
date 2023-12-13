<template>
  <div>
    <h1>云端的学习场景</h1>
    <div v-for="(person, index) in cloud" :key="index" class="person-card">
      <h3>{{ person.kind }}</h3>
      <p><strong>ID:</strong> {{ person.id }}</p>
      <p><strong>创建时间:</strong> {{ person.time }}</p>
      <hr>
    </div>
  </div>
  <hr />
  <br />
  <div>
    <h1>暂存的学习场景</h1>
    <div v-for="(person, index) in local" :key="index" class="person-card">
      <h3>{{ person.kind }}</h3>
      <p><strong>ID:</strong> {{ person.id }}</p>
      <p><strong>创建时间:</strong> {{ person.time }}</p>
      <hr>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cloud: [
        { kind: "二叉搜索树", id: 'user_0001_202311201233', time: '2023-11-20'},
        { kind: "图的遍历", id: 'user_0001_202311151425', time: '2023-11-15'}
      ],
      local: [
        { kind: "字符串匹配", id: 'user_0001_202311131751', time: '2023-11-13'}
      ]
    };
  }
};
</script>

<style scoped>
.person-card {
  border: 1px solid #ccc;
  padding: 10px;
  margin-bottom: 20px;
}
</style>
