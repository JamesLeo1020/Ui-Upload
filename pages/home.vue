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
                <td><img class="images" src="https://www.waterymouthcafe.co.nz/wp-content/uploads/2017/07/The-insiders-guide-to-great-coffee-from-the-baristas-at-Watery-Mouth-cafe-Blenheim1-500x500.jpg"></td>
                <td class="align-middle">Gayo Long Black</td>
                <td Class="align-middle">1231</td>
                <td class="align-middle">coffee shot mix with hot water</td>
                <td class="align-middle">19 juli 2021</td>
                <td class="btn-table"> <b-dropdown id="dropdown" icon="" class="m-md-2" variant="outline-dark">
                      <b-dropdown-item>Edit</b-dropdown-item>
                      <b-dropdown-divider></b-dropdown-divider>
                      <b-dropdown-item>Delete</b-dropdown-item>
                      </b-dropdown></td>
              </tr>
              <tr>
                <td><img class="images" src="data:image/jpeg;base64,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"></td>
                <td class="align-middle">Toraja Piccolo</td>
                <td Class="align-middle">1232</td>
                <td class="align-middle">15- 20 ml ristretto shot and 100ml steamed milk</td>
                <td class="align-middle">19 juli 2021</td>
                <td class="btn-table"> <b-dropdown id="dropdown" icon="" class="m-md-2" variant="outline-dark">
                      <b-dropdown-item>Edit</b-dropdown-item>
                      <b-dropdown-divider></b-dropdown-divider>
                      <b-dropdown-item>Delete</b-dropdown-item>
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