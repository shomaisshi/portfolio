<template>
  <div class="container" v-for="item in items" :key="item.title">
    <img class="image" v-bind:src="item.image" alt="content image" />
    <div class="iconContainer">
      <img class="icon" v-bind:src="item.icon" alt="content icon" />
      <div class="mainContainer">
        <div class="titleContainer">
          <h1 class="title">{{ item.title }}</h1>
          <span class="date">{{ item.date }}</span>
        </div>
        <details>
          <summary>
            {{ item.description }}
          </summary>
          <p>{{ item.moreDescription }}。</p>
        </details>
      </div>
    </div>
  </div>
</template>

<script>
const items = [
  {
    title: "Finger book",
    image: "https://placehold.jp/600x324.png",
    icon: "https://placehold.jp/64x64.png",
    date: "2018.4",
    description: "こんな作品です",
    moreDescription: "もっとこうです",
  },
  {
    title: "Portfolio",
    image: "https://placehold.jp/600x324.png",
    icon: "https://placehold.jp/64x64.png",
    date: "2021.4",
    description: "こんな作品です",
    moreDescription: "もっとこうです",
  },
  {
    title: "test",
    image: "https://placehold.jp/600x324.png",
    icon: "https://placehold.jp/64x64.png",
    date: "2021.8",
    description: "こんな作品です",
    moreDescription: "もっとこうです",
  },
];

export default {
  data() {
    return {
      items: items,
    };
  },
};
</script>

<style scoped>
.container {
  max-width: 600px;
  margin: 0 auto;
  padding: 8px;
}

.container + .container {
  margin-top: 32px;
}

.iconContainer {
  display: flex;
  align-items: flex-start;
  margin-top: 8px;
}

.mainContainer {
  margin-left: 16px;
  width: 100%;
}

.titleContainer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.image {
  width: 100%;
  height: 324px;
  object-fit: cover;
}

.icon {
  width: 64px;
  height: 64px;
  border-radius: 50%;
}

.title {
  font-size: 24px;
  margin: 0;
}

.date {
  font-size: 14px;
}
</style>