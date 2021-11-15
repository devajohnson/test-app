<template>
  <nav>
      <li
        v-for="(crumb,ci) in crumbs"
        :key="ci"
        class="breadcrumb-item align-items-left"
      >
        <button class="btn btn-link" :class="{ disabled: isLast(ci) }" @click="selected(crumb)">
          {{  }}
        </button>
      </li>
  </nav>
</template>

<script>
export default {
  props: {
    crumbs: {
      type: Array,
      required: true,
    },
  },
  methods: {
    isLast(index) {
      return index === this.crumbs.length - 1;
    },
    selected(crumb) {
      this.$emit('selected', crumb);
    },
  },
};
</script>
 
<style scoped>
.Projectbc {
  background-color: white;
  border: 1px solid rgba(0, 0, 0, 0.125);
  border-radius: 0.30rem;
}
</style>