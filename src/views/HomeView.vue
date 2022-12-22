<template>
  <h1>Belajar Form dan Vue Event</h1>
  <form>
  <div class="mb-3">
    <label for="exampleInputEmail1" class="form-label">Nama</label>
    <input v-model="nama" text="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
  </div>
  <div class="mb-3">
    <label for="exampleInputPassword1" class="form-label">NIM</label>
    <input v-model="nim" text="password" class="form-control" id="exampleInputPassword1">
  </div>
  
  <button type="submit" class="btn btn-primary" @click.prevent="simpanData">Submit</button> 
</form>

<hr>
<table class="table">
  <thead>
    <tr>
      <th>Nama</th>
      <th>Nim</th>
    </tr> 
  </thead>
  <tbody>
    <tr v-for="item in dataMahasiswa">
      <td>{{item.nama}}</td>
      <td>{{item.nim}}</td>
    </tr>
  </tbody>
</table>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
