<template>
  <div class="hello">
    <b-container>
      <b-row>
        <b-col>
          <h1>Practice Log</h1>
        </b-col>
      </b-row>
      <b-row>
        <b-col
          cols="4">
          <b-card no-body class="mb-1"
            header="Add Assignment">
            <b-card-body>
              <b-form @submit="onSubmit">
                <b-form-input id="exampleInput1"
                    label="Title"
                    type="text"
                    required
                    placeholder="Enter title">
                </b-form-input>
                <b-button type="submit" class="mt-2" block variant="primary">Submit</b-button>
              </b-form>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col
          cols="8">
          <b-card title="Assignment 1"
            tag="article"
            class="mb-2">
            <b-button href="www.google.com" variant="primary">Go somewhere</b-button>
          </b-card>
        </b-col>
      </b-row>      
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      user: 'Dylan',
      skillBank: [intonation, articulation, timing],
      form: {
        title: ""
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
