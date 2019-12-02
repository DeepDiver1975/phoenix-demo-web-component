<template>
  <section>
    <h1>The selected file:</h1>
    <div>{{ selectedFileParsed.id }}</div>
    <div>{{ selectedFileParsed.name }}</div>
    <div>{{ selectedFile }}</div>
  </section>
</template>

<script>
export default {
  props: ['selectedFile'],
  mounted () {
    console.log(this.selectedFile)
  },
  computed: {
    selectedFileParsed () {
      return JSON.parse(this.selectedFile)
    }
  }
}
</script>

<style>
h1 {
  color: green;
}
section {
  background-color: oldlace;
  margin-bottom: 4rem;
}
</style>
