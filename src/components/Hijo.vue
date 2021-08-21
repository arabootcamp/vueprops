<template>
  <div>
    <div class="d-inline-block text-center my-5">
      <h2 class="text-secondary">Lista</h2>
      <ul class="my-5">
        <li class="text-start mt-2" v-for="(item,index) in array" :key="index">{{item}}
          <button class="my-btn" v-on:click="deleteItem(index)">Eliminar</button>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Hijo',
    props: {
      array: Array
    },
    methods: {
      deleteItem(index) {
        this.$emit('pleaseDeleteIndex', index);
      }
    }
  }
</script>

<style scoped>
  .my-btn {
    display: inline-block;
    background-color: white;
    color: #DC3545;
    padding: 0px 20px;
    margin-left: 5px;
    border-radius: 10px;
    border: 2px solid #DC3545;
    font-size: 0.9rem;
    font-weight: 500;
  }

  .my-btn:hover {
    background-color: #DC3545;
    color: white;
  }
</style>