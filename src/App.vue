<template>
  <div class="container mt-5 mb-5">
    <div class="row">
      <div class="col mx-2 px-2 py-3 bg-light border rounded">
        <h6>Form attributes</h6>
        <draggable class="draggable-list" :list="stuff.form_attribute" :group="{ name: 'stuff', pull: 'clone', put: false}">
          <div v-for="(form_attribute, i) in stuff.form_attribute" :key="i">
            <div class="bg-white mt-3 p-2 shadow border rounded">
              <p>{{ form_attribute }}</p>
            </div>
          </div>
        </draggable>
      </div>
      <div class="col mx-2 px-2 py-3 bg-light border rounded">
        <h6>Form area</h6>
        <draggable class="draggable-list" :list="stuff.form_area" group="stuff">
          <div v-for="(form_area, i) in stuff.form_area" :key="i">
            <div class="bg-white mt-3 p-2 shadow border rounded">
              <p>{{ form_area }}</p>
            </div>
          </div>
        </draggable>
      </div>
           
    </div>
  </div>
</template>

<script>
import draggable from "vuedraggable";
export default {
  components: {
    draggable,
  },
  data() {
    return {
      stuff: {
        form_attribute: ["Text area", "Checkbox","Radiobutton"],
        form_area: [],
      },
    };
  },
};
</script>

<style scoped>
h6 {
  font-weight: 700;
}
.col {
  height: 90vh;
  overflow: auto;
}
.draggable-list {
  min-height: 10vh;
}
.draggable-list > div {
  cursor: pointer;
}
</style>