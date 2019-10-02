<template>
  <div class="prompt_wrapper">
    <div class="prompt">
      <mark :class="this.promptColor">{{ this.promptText }}</mark>
    </div>
  </div>
</template>

<script>
export default {
  name: "PromptText",
  computed: {
    promptColor: () => {
      let colors = ["turquoise", "blue", "red", "yellow", "green", "purple"];
      return colors[Math.floor(Math.random() * colors.length)];
    },
    promptText: () => {
      let prompts = ["$", ">", "#"];
      return prompts[Math.floor(Math.random() * prompts.length)];
    }
  }
};
</script>

<style>
.prompt_wrapper {
  flex-direction: row;
}
.prompt {
  flex-direction: column;
}
mark.turquoise {
  color: #56b6c2;
  background: none;
}
mark.blue {
  color: #61afef;
  background: none;
}
mark.yellow {
  color: #d19a66;
  background: none;
}
mark.red {
  color: #e06c75;
  background: none;
}
mark.green {
  color: #98c379;
  background: none;
}
mark.purple {
  color: #c678dd;
  background: none;
}
</style>
