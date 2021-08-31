<template>
<div>
<side-bar/>
<h2 class="header">Create Post</h2>
<div class="container-post">
  <div class="conpreview">

  </div>
  <div class="condropzone">
    <!-- <div id="wrapper">
      <input type="file" accept="image/*" onchange="preview_image(event)">
      <img id="output_image"/>
    </div>
  </div> -->

  <!-- <form action="/file-upload"
      class="dropzone"
      id="my-awesome-dropzone"></form>
  </div> -->

<!-- <main class="col s12">
  <div class="row">
    <form action="upload.php" id="zdrop" class="fileuploader centre-allign">
      <div id="upload-label" style="width: 200px">
        <i class="uil uil-upload"></i>
      </div>
      <span class="tittle">Click Button or Drop File Here</span>
    </form>

    <div class="preview-container">
      <div class="collection card" id="previews">
        <div class="collection-item clearhack valign-wrapper item-template" id="zdrop-template">
          <div class="left pv zdrop-info" data-dz-thumnail>
            <div>
              <span data-dz-name></span> <span data-dz-size></span>
            </div>
            <div class="progress">
              <div class="determinate" style="width:0" data-dz-uploadprogress></div>
            </div>
            <div class="dz-error-message">
              <span data-dz-error-message></span>
            </div>
            <div class="secondary-content actions">
              <a href="#!" data-dz-remove class="btn-floating ph red white-text waves-effect waves-light"><i class="material-icons white-text">clear</i></a>
            </div>
          </div>

        </div>

      </div>

    </div>

  </div>

</main> -->

<dropzone id="foo" ref="el" :options="options" :destroyDropzone="true">
  <div class="dropzone-custom-content">
                <h3 class="dropzone-custom-title">Custom slot</h3>
                <p class="subtitle">Subtitle</p>
                </div>
</dropzone>

</div>

<div class="productname">
  <h4>Product Name:</h4>
            <input
              v-model="ProductName"
              type="text"
              class="form-control"
              placeholder="Enter Here"
              required
            />
          </div>

<div class="idnumber">
  <h4>Id Number:</h4>
            <input
              v-model="IdNumber"
              type="number"
              class="form-control"
              placeholder="Enter Here"
              required
            />
          </div>

<div class="description">
  <h4>Description</h4>
            <input
              v-model="Description"
              type="text"
              class="form-control"
              placeholder="Enter Here"
              required
            />
          </div>

<div class="button-draft d-flex">
    <button type="button" class="btn btn-draft btn-info d-flex mr-2"><i class="uil uil-file-alt"></i> Draft</button>
    <button type="button" class="btn btn-publish btn-primary d-flex"><i class="uil uil-location-arrow"></i> Publish</button>

</div>


</div>
</div>
</template>

<script>
import sideBar from '../components/side-bar.vue'
import Dropzone from 'nuxt-dropzone'
import 'nuxt-dropzone/dropzone.css'
export default {
  components: {
    Dropzone
  },
  data() {
    return {
      // See https://rowanwins.github.io/vue-dropzone/docs/dist/index.html#/props
      options: {
        url: "http://httpbin.org/anything"
      }
    }
  },
  mounted() {
    // Everything is mounted and you can access the dropzone instance
    const instance = this.$refs.el.dropzone
  }
}
// function preview_image(event) 
// {
//  var reader = new FileReader();
//  reader.onload = function()
//  {
//   var output = document.getElementById('output_image');
//   output.src = reader.result;
//  }
//  reader.readAsDataURL(event.target.files[0]);
// }

</script>

<style>

</style>