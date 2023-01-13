<script>
export default {
    data () {
        return {
            activeItem: 0,
            menu: [
                {
                    label: 'CHARACTERS',
                    url: '#',
                    active: false
                },
                {
                    label: 'COMICS',
                    url: '#',
                    active: true
                },
                {
                    label: 'MOVIES',
                    url: '#',
                    active: false
                },
                {
                    label: 'TV',
                    url: '#',
                    active: false
                },
                {
                    label: 'GAMES',
                    url: '#',
                    active: false
                },
                {
                    label: 'VIDEO',
                    url: '#',
                    active: false
                },
                {
                    label: 'FANS',
                    url: '#',
                    active: false
                },
                {
                    label: 'NEWS',
                    url: '#',
                    active: false
                },
                {
                    label: 'SHOP',
                    url: '#',
                    active: false
                },
            ]
        }
    },
    methods: {
        selectedItem(index) {
            this.activeItem = index
            }
    }
}
</script>

<template lang="">
  <header class="container">
        <a href="/" class="logo">
            <img src="/img/dc-logo.png" alt="logo-dc">
        </a>
        <nav>
              <ul>
                  <li v-for="(item, index) in menu" :key="index" @click="selectedItem(index)" :class="(activeItem === index) ? 'active' : ''">
                      <a :href="item.url">
                          {{ item.label }}
                      </a>
                  </li>
              </ul>
         </nav>
  </header>
</template>

<style lang="scss" scoped>
@use '../styles/generals.scss' as *;
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

  header {
    text-align: center;
    align-items: center;
    @include justify_between;

    img {
        width: 80%;
    }

    ul {
        list-style: none;
        margin-top: 2rem;
        @include justify_center;

        .active {
            color: $primary;
            border-bottom: 3px solid $primary;
            padding-bottom: 2em;
        }

        li {
            height: 100%;
            padding: 1rem;
            font-size: 16px;
        }
  }
}
</style>