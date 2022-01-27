<template>
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
        form_area: [],
      },
    };
  },
};
</script>