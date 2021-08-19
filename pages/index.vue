<template>
  <div>
    <div class="content">
      <div class="inner">
        <div class="top-div">
          <h6>User Details</h6>
          <button class="add-btn">
            <img src="~/assets/Plus.svg" alt="" /> Add New User
          </button>
        </div>
        <div class="input-row">
          <div class="input-container">
            <label>First Name</label>
            <input v-model="first_name" type="text" />
          </div>
          <div class="input-container">
            <label>Last Name</label>
            <input v-model="last_name" type="text" />
          </div>
        </div>
        <div class="input-row">
          <div class="input-container">
            <label>Email Address</label>
            <input v-model="email_address" type="text" />
          </div>
          <div class="input-container">
            <label>Gender</label>
            <input v-model="gender" type="text" />
          </div>
        </div>
        <div class="input-row">
          <div class="input-container">
            <label>Phone Number</label>
            <input v-model="number" type="text" />
          </div>
          <div class="input-container">
            <label>Age</label>
            <input v-model="age" type="text" />
          </div>
        </div>
        <div class="input-row">
          <div class="input-container">
            <label>Language</label>
            <input v-model="language" type="text" />
          </div>
          <div class="input-container">
            <label>State</label>
            <input v-model="state" type="text" />
          </div>
        </div>
        <div class="save-btn">
          <button @click="showModal = true">Save</button>
        </div>
      </div>
    </div>
    <SavedModal v-show="showModal" @close-modal="showModal = false" />
  </div>
</template>

<script>
import SavedModal from '~/components/SavedModal.vue'

export default {
  components: { SavedModal },
  data() {
    return {
      showModal: false,
      first_name: '',
      last_name: '',
      email_address: '',
      gender: '',
      number: '',
      age: '',
      language: '',
      state: '',
    }
  },
}
</script>

<style scoped>
.content {
  padding: 150px;
}

.inner {
  margin: auto;
  width: 65%;
}

.top-div {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 50px;
}

.add-btn {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 20px;
  border-radius: 10px;
  width: 160px;
}

h6 {
  font-size: 25px;
  font-weight: 500;
}

button {
  background-color: #ac003e;
  width: 150px;
  height: 40px;
  color: white;
  font-size: 14px;
  border-radius: 16px;
}

label {
  margin-bottom: 10px;
}

input {
  border: 1px solid #00000041;
  height: 40px;
  padding: 10px;
  border-radius: 8px;
  width: 400px;
}

.input-row {
  display: flex;
  justify-content: space-between;
}

.input-container {
  display: flex;
  flex-direction: column;
  margin-bottom: 30px;
}

.save-btn {
  text-align: center;
  margin-top: 50px;
}
</style>
