<script>
import ContactCard from "@/components/ContactCard.vue";

export default {
  data() {
    return {
      contacts: [
        {id: 1, name: "Santi", phone: "02934785", email: "asss@sd.com"},
        {id: 2, name: "Laia", phone: "02934785", email: "asss@sd.com"},
        { id: 3, name: "Jordi", phone: "02934785", email: "asss@sd.com"},
      ]
    }
  },
  components: {
    ContactCard
  }
};
</script>

<template>
  <div>
    <h1>Start here for the components exercise</h1>
    <section>
      <ul>
        <ContactCard v-for="contact in contacts" :name="contact.name" :phone="contact.phone" :email="contact.email"/>
      </ul>
    </section>
  </div>
</template>

<style scoped>
ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.card {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem auto;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
  width: 100%;
  max-width: 40rem;
}

h2 {
  font-size: 2rem;
  border-bottom: 4px solid #ccc;
  color: #58004d;
  margin: 0 0 1rem 0;
}

button {
  font: inherit;
  cursor: pointer;
  border: 1px solid #ff0077;
  background-color: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
}

button:hover,
button:active {
  background-color: #ec3169;
  border-color: #ec3169;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.26);
}
</style>