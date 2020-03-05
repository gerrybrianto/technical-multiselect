<script>
export default {
  name: 'Multiselect',
  props: {
    options: {
      type : Array,
      default: () => [],
      required: true,
    },
    placeholder: {
      type: String,
      default: 'Je suis le placeholder',
      required: false,
    }
  },
  data() {
    return {

    }
  },
  computed: {

  },
  methods: {
    onSelectPress() {
      alert('Oh, ça alors, tu m\'as cliqué dessus !')
    }
  }
}
</script>

<template>
  <div class="multiselect" @click="onSelectPress">
    {{ placeholder }}
    <!-- 
      Tout est à construire ici...
      Bonne chance 😉
     -->
  </div>
</template>

<style lang="scss" scoped>
.multiselect {
  min-width: 300px;
  min-height: 40px;
  border-radius: 5px;
  border: 1px solid black;
  display: flex;
  align-items: center;
  padding: 10px;

  &:hover {
    cursor:pointer;
  }
}
</style>
