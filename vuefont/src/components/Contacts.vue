<template>
 <div class="contacts">
  <p>toan</p>
  <div v-for="contact in contacts" :key="contact.id">
   <p>{{contact.name}} is my {{contact.relationship}}</p>
  </div>
 </div>
</template>
<script>
import axios from 'axios'
export default {
  name: 'Contacts',
  data () {
    return {
      contacts: [],
      name: [],
      relationship: [],
      errors: []
    }
  },
  created () {
    axios.get('http://localhost:3000/contacts')
      .then(response => {
        this.contacts = response.data
        console.log(response.data)
      })
      .catch(e => {
        this.error.push(e)
      })
  }
}
</script>
