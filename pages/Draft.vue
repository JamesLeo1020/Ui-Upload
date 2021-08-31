<template>
<div>
<side-bar/>
<div>
<h2 class="header">Home</h2>
<div class="container-home">
  <nav class="search-box">
<form class="form-inline">
  <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
  <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>

<div>
  <b-dropdown id="dropdown-1" text="Short By" class="m-md-2" variant="outline-dark">
    <b-dropdown-item>Id Number</b-dropdown-item>
    <b-dropdown-divider></b-dropdown-divider>
    <b-dropdown-item>Name</b-dropdown-item>
  </b-dropdown>
</div>

</form>
</nav>
  <div class="col-md ml-5">
    <div class="card">
      <div class="card-body">
        <table class="table col-12">
          <thead>
            <tr>
              <th scope="col">Images</th>
              <th scope="col">Product</th>
              <th scope="col">ID Number</th>
              <th scope="col">Description</th>
              <th scope="col">Date Publish</th>
              <th scope="col"></th>
            </tr>
          </thead>
          <tbody class="inside-table">
              <tr>
                <td><img class="images" src="https://www.bakefromscratch.com/wp-content/uploads/2017/04/ORIGINOFACLASSIC500JB-696x557.jpg"></td>
                <td class="align-middle">New York Cheese Cake</td>
                <td Class="align-middle">1233</td>
                <td class="align-middle">New York cheesecake has a dense texture but feels smoother</td>
                <td class="align-middle">-</td>
                <td class="btn-table"> <b-dropdown id="dropdown" icon="" class="m-md-2" variant="outline-dark">
                      <b-dropdown-item>Publish</b-dropdown-item>
                      <b-dropdown-divider></b-dropdown-divider>
                      <b-dropdown-item>Edit</b-dropdown-item>
                      </b-dropdown></td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>

    <!-- <div class="table">
    <b-table striped hover :items="items" :fields="fields"></b-table>
  </div> -->
  </div>
  </div>
</div>
</template>

<script>
import sideBar from '../components/side-bar.vue'
export default {
// data() {
//   return {
//         // Note `isActive` is left out and will not appear in the rendered table
//         fields: ['product', 'id_number', 'description', 'date_publish'],
//         items: [
//           { product: 'Long Black', id_number:'1231', description:'Coffee Shot mix with hot water', date_publish:'19 july 2021'},
//         ]
//       }
// }
}
</script>

<style>

</style>