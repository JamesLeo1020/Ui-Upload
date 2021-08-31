<template>
<div>
<side-bar/>
<h2 class="header">Create Post</h2>
<div class="container-post">
  <div class="conpreview">
          <!-- <div class="border p-2 mt-3"> -->
            <!-- <p>Preview Here:</p>
            <template v-if="preview">
              <img :src="preview" class="img-fluid" />
              <p class="mb-0">file name: {{ image.name }}</p>
              <p class="mb-0">size: {{ image.size/1024 }}KB</p>
            </template> -->
          <!-- </div> -->
          <div class="border p-2 mt-3">
            <p>Preview Here:</p>
            <template v-if="preview_list.length">
              <div v-for="item, index in preview_list" :key="index">
                <img :src="item" class="img-fluid" />
                <p class="mb-0">file name: {{ image_list[index].name }}</p>
                <p>size: {{ image_list[index].size/1024 }}KB</p>
              </div>
            </template>
          </div>
  </div>
  <div class="condropzone">


<!-- <dropzone id="foo" ref="el" :options="options" :destroyDropzone="true">
    <div class="dropzone-custom-content">
          <h3 class="dropzone-custom-title">Custom slot</h3>
        <p class="subtitle">Subtitle</p>
    </div>
</dropzone> -->
    <!-- <div class="col-md-5 offset-md-1"> -->
      <h5>2. multiple file</h5>

      <form>
        <div class="form-group">
          <!-- <label for="my-file">Select Image</label>
          <input type="file" accept="image/*" @change="previewImage" class="form-control-file" id="my-file">
     -->
          <label for="my-file">Select Image</label>
          <input type="file" accept="image/*" multiple="multiple" @change="previewMultiImage" class="form-control-file" id="my-file">

        </div>
      </form>
      
    <!-- </div> -->

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
// import Dropzone from 'nuxt-dropzone'
import 'nuxt-dropzone/dropzone.css'
export default {
  components: {
    // Dropzone
  },
  data() {
    return {
      preview: null,
      image: null,
      preview_list: [],
      image_list: [],
      // See https://rowanwins.github.io/vue-dropzone/docs/dist/index.html#/props
      options: {
        url: "http://httpbin.org/anything"
      }
      
    }
  },
  // mounted() {
  //   // Everything is mounted and you can access the dropzone instance
  //   const instance = this.$refs.el.dropzone
  // },
  methods: {
      previewImage: function(event) {
      var input = event.target;
      if (input.files) {
        var reader = new FileReader();
        reader.onload = (e) => {
          this.preview = e.target.result;
        }
        this.image=input.files[0];
        reader.readAsDataURL(input.files[0]);
      }
    },
    previewMultiImage: function(event) {
      var input = event.target;
      var count = input.files.length;
      var index = 0;
      if (input.files) {
        while(count --) {
          var reader = new FileReader();
          reader.onload = (e) => {
            this.preview_list.push(e.target.result);
          }
          this.image_list.push(input.files[index]);
          reader.readAsDataURL(input.files[index]);
          index ++;
        }
      }
    },
    reset: function() {
      this.image = null;
      this.preview = null;
      this.image_list = [];
      this.preview_list = [];
    }
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