<template>
  <div>
    <mdc-card>
      <mdc-card-header
        subtitle='subtitle here'
        title='Title goes here'
      ></mdc-card-header>
      <mdc-card-primary-action>
        <mdc-card-media :src='card'></mdc-card-media>
      </mdc-card-primary-action>

      <mdc-card-actions>
        <mdc-card-action-buttons>
          <mdc-card-action-button>ACTION</mdc-card-action-button>
        </mdc-card-action-buttons>
        <mdc-card-action-icons>
          <mdc-card-action-icon icon='star'/>
        </mdc-card-action-icons>
      </mdc-card-actions>
    </mdc-card>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      msg: "Welcome to Your Vue.js App"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
