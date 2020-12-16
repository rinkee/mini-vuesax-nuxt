<template>
  <div class="">
    <div class="text-center">
      <input
        class="w-2/3 h-12 bg-gray-200 text-gray-700 rounded shadow-md mt-10 px-4"
        placeholder="Search"
        type="text"
      />
    </div>
    <section class="mt-20">
      <h1 class="text-2xl text-gray-700 font-semibold">모집중인 프로젝트</h1>
      <div class="flex flex-wrap">
        <div v-for="item in items" :key="item.index" class="card m-1">
          <img class="w-full rounded-lg" src="@/assets/img/1.jpeg" alt="" />
          <p class="text-sm text-gray-600">{{ item.dev }}</p>
          <h2 class="text-sm text-gray-800">{{ item.title }}</h2>
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component({})
export default class MyClass extends Vue {
  data() {
    return {
      items: [
        {
          dev: 'APP',
          title: '계획부터 런칭까지 같이 시작하실 분 구합니다.',
          img: '@/assets/img/1.jpeg',
        },
        {
          dev: 'APP',
          title: '계획부터 런칭까지 같이 시작하실 분 구합니다.',
          img: '@/assets/img/2.jpeg',
        },
        {
          dev: 'APP',
          title: '계획부터 런칭까지 같이 시작하실 분 구합니다.',
          img: '@/assets/img/3.jpeg',
        },
        {
          dev: 'APP',
          title: '계획부터 런칭까지 같이 시작하실 분 구합니다.',
          img: '@/assets/img/4.jpeg',
        },
      ],
    }
  }
}
</script>

<style>
.card {
  width: calc(50% - 10px);
}
.img-wh {
  width: 224px;
  height: 224px;
}
</style>
