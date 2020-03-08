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
    },
    tags: {
      type: Array,
      default: () => [],
      required: true
    }
  },
  data() {
    return { state: false };
  },
  computed: {},
  methods: {
    onSelectPress() {
      console.log("Select");
      if (this.state) {
        this.state = false;
      } else {
        this.state = true;
      }
    },

    onOptionsPress(item) {
      console.log("Option " + item + typeof item);
      this.state = false;
      this.addTags(item);
    },

    addTags(tag) {
      if (typeof tag === "string") {
        this.tags.push(tag);
        this.options.splice(this.options.indexOf(tag), 1);
      } else {
        return console.error("Tag invalide");
      }
    },

    removeTags(tagIndex) {
      if (typeof tagIndex === "number") {
        if(!this.state){
          this.state = true;
        }
        this.options.unshift(this.tags[tagIndex]);
        this.tags.splice(tagIndex, 1);
      } else {
        return console.error("Index invalide");
      }
    }
  }
};
</script>

<template>
  <div class="multiselect">
    <div @click="onSelectPress" class="multiselect_tags">
      <ul v-if="tags.length != 0">
        <li v-for="item in tags " :key="tags.indexOf(item) * 10">
          {{ item }}
          <button @click="removeTags(tags.indexOf(item))">X</button>
        </li>
      </ul>
      <span v-else>{{ placeholder }}</span>
    </div>
    <div class="multiselect_content">
      <ul v-if="state">
        <li
          v-for="item in options"
          :key="options.indexOf(item)"
          @click="onOptionsPress(item)"
        >{{ item }}</li>
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

  .multiselect_tags {
    border: 1px solid black;
  }
  .multiselect_content ul {
    border: 1px solid black;
    list-style-type: none;
  }

  .multiselect_content li {
    border: 1px solid black;
    padding-bottom: 10%;
  }
  .multiselect_content li span {
    border: 1px solid black;
  }

  &:hover {
    cursor: pointer;
  }
}
</style>
