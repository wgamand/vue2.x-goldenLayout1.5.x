<template>
  <vue-golden-layout
  :config="config"
  :scroll="scroll"
  > 
  <another></another>
  </vue-golden-layout>
</template>

<script>
import Another from "../essentials/row/Another";
export default {
  name: "PanelScrolling",
  components: { Another },
  data() {
    return {
      scroll: true,
      config: {
        content: [
          {
            type: "row",
            content: [
              {
                type: "component",
                componentName: "ComponentA",
                componentState: { text: "Another" },
              },
              {
                type: "column",
                content: [
                  {
                    type: "component",
                    componentName: "ComponentB",
                  },
                  {
                    type: "component",
                    componentName: "ComponentC",
                  },
                ],
              },
            ],
          },
        ],
      },
    };
  },


};
</script>

<style>
</style>