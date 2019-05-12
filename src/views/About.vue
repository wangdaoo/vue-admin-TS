<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h1>{{ fullName }}</h1>
  </div>
</template>
<script>
export default {
  data () {
    return {
      firstName: 'Mars',
      lastName: 'Wong'
    }
  },
  computed: {
    // fullName: function () {
    //   return this.firstName + this.lastName
    // }
    fullName: {
      get: function () {
        return this.lastName + ' ' + this.firstName
      },

      set: function (newVal) {
        console.log(newVal)
        let names = newVal.split(' ')
        this.firstName = names[0]
        this.lastName = names[names.lenght - 1]
      }
    }
  },
  methods: {
  }
}
</script>
