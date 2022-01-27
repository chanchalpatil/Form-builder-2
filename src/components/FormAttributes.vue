<template>
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
        form_attribute: ["Text area", "Checkbox","Radiobutton"]
      },
    };
  },
};
</script>
