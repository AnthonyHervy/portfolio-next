<template>
  <div class="center grid" style="padding-top: 50px">
    <vs-row justify="space-around">
      <vs-card
        v-for="card in cards"
        :key="card.id"
        vs-type="flex"
        vs-justify="center"
        vs-align="center"
        type="5"
      >
        <template #title>
          <h3>{{ card.title }}</h3>
        </template>
        <template #img>
          <img :src="card.img" alt="" />
        </template>
        <template #text>
          <p>{{ card.desc }}</p>
        </template>
        <template #interactions>
          <vs-button icon shadow :href="card.repo" blank>
            <i class="bx bxl-github"></i>
          </vs-button>
          <vs-button danger icon :to="card.route">
            <i class="bx bx-arrow-to-right"></i>
          </vs-button>
        </template>
      </vs-card>
    </vs-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          id: 1,
          title: 'React Starter',
          desc: 'This is a React template with CLI, to boostrap projects',
          img: 'https://i.imgur.com/8MwoGki.png',
          repo: 'https://github.com/Karnak19/react-starter-wcs',
          route: '/portfolio/react-starter',
        },
        {
          id: 2,
          title: 'KissBot',
          img:
            'https://raw.githubusercontent.com/Karnak19/kissBot/master/avatar.png',
          desc:
            'Discord bot, used to simplify our gaming team everyday workflow (event creation, team setup, strategies files, etc.)',
          repo: 'https://github.com/Karnak19/kissbot',
          route: '/portfolio/kissbot',
        },
        {
          id: 3,
          title: 'Title',
          desc:
            'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ad recusandae optio nam odit officiis consequatur, cumque magnam veniam exercitationem sapiente.',
          img: 'https://vuesax.com/foto13.png',
          repo: 'https://github.com/Karnak19/kissbot',
          route: '/portfolio/title',
        },
      ],
    }
  },
}
</script>

<style></style>
