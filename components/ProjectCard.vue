<template>
  <article
    class="w-100 h5 mb5 bg-white relative cover bg-center"
    v-bind:style="{backgroundImage: `url(${project.image})`}"
    :title="project.name"
  >
    <a :href="project.url" class="db w-100 h-100 link hide-child">
      <div class="f4 white w-100 h-100 pa3 bg-blue absolute top-0 left-0 child">
        {{project.description}}
      </div>
    </a>
  </article>
</template>

<script>
export default {
  name: 'ProjectCard',
  props: {
    'project': {
      type: Object,
      required: true,
    },
  },
}
</script>

<style scoped>
a h3 {
  text-align: center;
  line-height: 8rem;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}
@media screen and (min-width: 480px) {
  article {
    width: calc(45% - 10px);
  }
  article:nth-child(2n) {
    margin-right: 0;
  }
  article:nth-child(2n+1) {
    margin-right: 15px;
  }
}
</style>
