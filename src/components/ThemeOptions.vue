<template>
  <section>
    <div class="theme-option">
      <label for="themeOne">
        <h2>Theme One</h2>
        <input type="radio" id="themeOne" name="themeNumber" value="themeOne" />
        <div style="background: #39414b"></div>
        <div style="background: #1f2327"></div>
        <div style="background: #4ecca3"></div>
      </label>
    </div>
    <div class="theme-option">
      <label for="themeTwo">
        <h2>Theme Two</h2>
        <input type="radio" id="themeTwo" name="themeNumber" value="themeTwo" />
        <div style="background: #525252"></div>
        <div style="background: #313131"></div>
        <div style="background: #db5059"></div>
      </label>
    </div>
    <div class="theme-option">
      <label for="themeThree">
        <h2>Theme Three</h2>
        <input type="radio" id="themeThree" name="themeNumber" value="themeThree" />
        <div style="background: #faf5ef"></div>
        <div style="background: #d7d1c9"></div>
        <div style="background: #672f2f"></div>
      </label>
    </div>
    <div class="theme-option">
      <label for="themeFour">
        <h2>Theme Four</h2>
        <input type="radio" id="themeFour" name="themeNumber" value="themeFour" />
        <div style="background: #6e2142"></div>
        <div style="background: #943855"></div>
        <div style="background: #ffd692"></div>
      </label>
    </div>
  </section>
</template>

<script>
export default {
  name: "ThemeOptions"
};
</script>

<style lang="scss" scoped>
%toolbar-background {
  background: repeating-linear-gradient(
      -35deg,
      transparent,
      transparent 12px,
      var(--primaryOneTransparent) 12px,
      var(--accentTransparent) 24px
    ),
    linear-gradient(
      to bottom,
      var(--primaryOneTransparent),
      var(--accentTransparent)
    );
}

%menu-button {
  .menu-button {
    @extend %toolbar-background;
    padding: 16px;
    cursor: pointer;
    border-bottom: 4px solid var(--accent);
    box-shadow: 1px 2px 3px var(--primaryOneTransparent);
  }
}

%menu-content {
  .menu-content {
    margin: 16px;
  }
}

section {
  @extend %menu-button;
  @extend %menu-content;
  .theme-option {
    display: flex;
    justify-content: center;
    align-content: center;
    flex-direction: column;
    label {
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 4px -16px;
      padding: 2px 16px;
      flex-wrap: wrap;
      cursor: pointer;
      h2 {
        margin: 0;
        font-size: 1.25rem;
        flex-grow: 1;
        width: 100%;
      }
      div {
        display: inline-block;
        padding: 8px 17px;
        margin: 2px;
        border: 1px dashed black;
        border-radius: 4px;
        flex-grow: 1;
      }
      input {
        display: none;
        margin: 0 5px 0 0;
      }
      &:hover {
        background-color: var(--primaryOneTransparent);
      }
    }
  }
}
</style>