<template>
  <div class="forum">
    <h1>化学论坛 - 有机化学板块</h1>
    <div class="post">
      <h2>乙酸的结构式</h2>
      <!-- 化学公式展示 -->
      <div id="formula"></div>
      <p>乙酸（$CH_3COOH$）是一种有机一元酸，为食醋主要成分。</p>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import katex from 'katex'
import 'katex/dist/katex.min.css'

onMounted(() => {
  // 渲染复杂化学公式
  katex.render(
    'CH_3-COOH',
    document.getElementById('formula'),
    { displayMode: true }
  )
})
</script>

<style>
.forum { padding: 20px; max-width: 800px; margin: 0 auto; }
.post { margin-top: 20px; padding: 10px; border: 1px solid #eee; }
</style>