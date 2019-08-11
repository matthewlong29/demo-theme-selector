<template>
  <div id="app">
    <h1>Dark or Light Theme...</h1>
    <ThemeOptions />
    <p>Swat at dog meow meow mama so taco cat backwards spells taco cat or attack the child so take a big fluffing crap 💩 snuggles up to shoulders or knees and purrs you to sleep. Stare at imaginary bug the dog smells bad yet fall asleep on the washing machine terrorize the hundred-and-twenty-pound rottweiler and steal his bed, not sorry be a nyan cat, feel great about it, be annoying 24/7 poop rainbows in litter box all day so spread kitty litter all over house for demand to have some of whatever the human is cooking, then sniff the offering and walk away</p>
    <p>Lay on arms while you're using the keyboard allways wanting food. Have my breakfast spaghetti yarn sun bathe, for wack the mini furry mouse so attack the dog then pretend like nothing happened lick the plastic bag yet claw your carpet in places everyone can see - why hide my amazing artistic clawing skills? pet me pet me don't pet me. Leave fur on owners clothes i love cuddles, but lick arm hair or annoy owner until he gives you food say meow repeatedly until belly rubs.</p>
  </div>
</template>

<script>
import ThemeOptions from "@/components/ThemeOptions.vue";

export default {
  components: {
    ThemeOptions
  },
  mounted() {
    const toggleSwitch = document.querySelector(
      '.theme-switch input[type="radio"]'
    );
    const currentTheme = localStorage.getItem("theme");

    if (currentTheme) {
      document.documentElement.setAttribute("data-theme", currentTheme);

      if (currentTheme === "dark") {
        toggleSwitch.checked = true;
      }
    }

    function switchTheme(e) {
      if (e.target.checked) {
        document.documentElement.setAttribute("data-theme", "dark");
        localStorage.setItem("theme", "dark");
      } else {
        document.documentElement.setAttribute("data-theme", "light");
        localStorage.setItem("theme", "light");
      }
    }

    toggleSwitch.addEventListener("change", switchTheme, false);
  }
};
</script>

<style lang="scss">
:root {
  --primaryOne: rgb(57, 65, 75);
  --primaryOneTransparent: rgba(57, 65, 75, 0.15);
  --primaryTwo: rgb(31, 35, 39);
  --primaryTwoTransparent: rgba(31, 35, 39, 0.15);
  --accent: rgb(78, 204, 163);
  --accentTransparent: rgba(78, 204, 163, 0.15);
}
[data-theme="one"] {
  --primaryOne: rgb(57, 65, 75);
  --primaryOneTransparent: rgba(57, 65, 75, 0.15);
  --primaryTwo: rgb(31, 35, 39);
  --primaryTwoTransparent: rgba(31, 35, 39, 0.15);
  --accent: rgb(78, 204, 163);
  --accentTransparent: rgba(78, 204, 163, 0.15);
}
[data-theme="two"] {
  --primaryOne: rgb(82, 82, 82);
  --primaryOneTransparent: rgba(82, 82, 82, 0.15);
  --primaryTwo: rgb(49, 49, 49);
  --primaryTwoTransparent: rgba(49, 49, 49, 0.15);
  --accent: rgb(219, 80, 89);
  --accentTransparent: rgba(219, 80, 89, 0.15);
}
[data-theme="three"] {
  --primaryOne: rgb(250, 245, 239);
  --primaryOneTransparent: rgba(250, 245, 239, 0.15);
  --primaryTwo: rgb(215, 209, 201);
  --primaryTwoTransparent: rgba(215, 209, 201, 0.15);
  --accent: rgb(103, 47, 47);
  --accentTransparent: rgba(103, 47, 47, 0.15);
}
[data-theme="four"] {
  --primaryOne: rgb(110, 33, 66);
  --primaryOneTransparent: rgba(110, 33, 66, 0.15);
  --primaryTwo: rgb(148, 56, 85);
  --primaryTwoTransparent: rgba(148, 56, 85, 0.15);
  --accent: rgb(255, 214, 146);
  --accentTransparent: rgba(255, 214, 146, 0.15);
}

body {
  margin: 0 auto;
  background-color: var(--primaryTwo);
  color: var(--accent);
  max-width: 800px;
}

h1 {
  color: var(--primaryOne);
}

a {
  color: var(--accent);
}
</style>
