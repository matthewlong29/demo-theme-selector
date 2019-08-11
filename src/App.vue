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
      '.theme-switch input[type="checkbox"]'
    );

    function switchTheme(e) {
      if (e.target.checked) {
        document.documentElement.setAttribute("data-theme", "dark");
      } else {
        document.documentElement.setAttribute("data-theme", "light");
      }
    }

    toggleSwitch.addEventListener("change", switchTheme, false);
  }
};
</script>

<style lang="scss">
:root {
  --primary-color: #302ae6;
  --secondary-color: #536390;
  --accent-color: #66bb6a;
  --font-color: #424242;
  --bg-color: #fff;
  --heading-color: #292922;
}

[data-theme="dark"] {
  --primary-color: #9a97f3;
  --secondary-color: #818cab;
  --accent-color: #ae49bb;
  --font-color: #e1e1ff;
  --bg-color: #161625;
  --heading-color: #818cab;
}

body {
  margin: 0 auto;
  background-color: var(--bg-color);
  color: var(--font-color);
  max-width: 800px;
}

h1 {
  color: var(--secondary-color);
}

a {
  color: var(--primary-color);
}
</style>
