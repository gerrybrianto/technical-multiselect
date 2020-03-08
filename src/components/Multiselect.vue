<script>
export default {
  name: "Multiselect",
  props: {
    options: {
      type: Array,
      default: () => [],
      required: true
    },
    placeholder: {
      type: String,
      default: "Je suis le placeholder",
      required: false
    }
  },
  data() {
    return { state: false };
  },
  computed: {},
  methods: {
    onSelectPress() {
      if (this.state) {
        this.state = false;
      } else {
        this.state = true;
      }
    }
  }
};
</script>

<template>
  <div class="multiselect" @click="onSelectPress">
    <div class="multiselect_tags">{{ placeholder }}</div>
    <div class="multiselect_content">
      <ul v-if="state">
        <li v-for="item in options" :key="options.indexOf(item)">{{ item }}</li>
      </ul>
    </div>

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
  flex-direction: column;
  align-items: center;
  padding: 10px;

  .multiselect_content ul {
    list-style-type: none;
  }

  .multiselect_content li {
    padding-bottom: 10%;
  }

  &:hover {
    cursor: pointer;
  }
}
</style>
