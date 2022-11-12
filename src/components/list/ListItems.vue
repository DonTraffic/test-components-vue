<template>
  <v-container>
    <v-list flat>
      <v-list-item-group
        v-model="selectedItem"
        color="#ff7f50"
      >
        <ListItem v-for="item of info" :key='item.id' :info='item'/>
      </v-list-item-group>

    </v-list>
  </v-container>
</template>

<script>
  import ListItem from "./ListItem.vue";

  export default {
    name: 'ListTags',

    data() {
      return {
        selectedItem: '',
        
        info: [
          {
            title: 'Город сыра и мира',
            data: [
              {
                icon: 'mdi-star-outline',
                value: '5'
              },
              {
                icon: '',
                value: 'Историческая'
              },
              {
                icon: 'mdi-bus',
                value: 'На автобусе'
              },
              {
                icon: '',
                value: '28 марта'
              },
              {
                icon: 'mdi-clock-time-three-outline',
                value: '9'
              },

            ]

          },

          {
            title: 'Экскурсия в национальный паре "Куршская коса"',
            data: [
              {
                icon: 'mdi-star-outline',
                value: '5'
              },
              {
                icon: '',
                value: 'Обзорная'
              },
              {
                icon: 'mdi-bus',
                value: 'На автобусе'
              },
              {
                icon: '',
                value: '25 марта'
              },
              {
                icon: 'mdi-clock-time-three-outline',
                value: '6'
              },
              
            ]
            
          },

          {
            title: '"О кирках, рыщарях и замках"',
            data: [
              {
                icon: 'mdi-star-outline',
                value: '5'
              },
              {
                icon: '',
                value: 'Историческая'
              },
              {
                icon: 'mdi-bus',
                value: 'На автобусе'
              },
              {
                icon: '',
                value: '29 марта'
              },
              {
                icon: 'mdi-clock-time-three-outline',
                value: '6'
              },
              
            ]
            
          },

          {
            title: 'Экскурсия в Янтарный',
            data: [
              {
                icon: '',
                value: 'Историческая'
              },
              {
                icon: 'mdi-bus',
                value: 'На автобусе'
              },
              {
                icon: '',
                value: '29 марта'
              },
              {
                icon: 'mdi-clock-time-three-outline',
                value: '6'
              },
              {
                icon: 'mdi-account',
                value: 'до 49'
              },
              
            ]
            
          },

        ]

      }

    },

    components: {ListItem}

  }
</script>
