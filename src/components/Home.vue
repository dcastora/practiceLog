<template>
  <div class='hello'>
    <b-container>
      <b-row>
        <b-col>
          <h1>Practice Log</h1>
        </b-col>
      </b-row>
      <b-row>
        <b-col
          cols='4'>
          <b-card no-body class='mb-1'
            header='Add Assignment'>
            <b-card-body>
              <b-form @submit='onSubmit'>
                <b-form-input id='title'
                  label='Title'
                  type='text'
                  required
                  v-model='title'
                  placeholder='Enter Title'>
                </b-form-input>
                <b-form-input id='composer'
                  class='mt-2'
                  label='composer'
                  type='composer'
                  required
                  v-model='composer'
                  placeholder='Enter Composer'>
                </b-form-input>
                <b-button type='submit' class='mt-2' block variant='primary'>Submit</b-button>
              </b-form>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col
          cols='8'>
          <b-card v-for='assignment in assignments' :key='assignment.id'
            :title='assignment.title'
            bg-variant='success'
            text-variant='white'
            class='mb-3'>
            <p class="card-text">{{ assignment.composer }}</p>
          </b-card>
        </b-col>
      </b-row>      
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'main',
  data () {
    return {
      user: 'Dylan',
      skillBank: ['intonation', 'articulation', 'timing'],
      assignments: [],
      title: '',
      composer: ''
    }
  },
  methods: {
    onSubmit () {
      let newAssignment = {
        title: this.title,
        composer: this.composer,
        id: this.assignments.length + 1
      }
      this.assignments.push(newAssignment)
      console.log('yes')
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
