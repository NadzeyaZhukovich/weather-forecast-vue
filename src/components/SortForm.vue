<template>
  <section class="sort-form weather-content__sort">
          <h2 class="visually-hidden">Sort form</h2>
  <form action="#" method="GET">
    <div class="sort-form__group">
      <div class="sort-form__input-wrapper input-wrapper input-wrapper--search">
        <input id="search" type="search"
               name="city-search"
               placeholder="ity name"
               v-model="city"
               v-on:keydown.enter.prevent="$emit('onCityEntered', city)" />
        <label for="search" aria-label="Search"></label>
      </div>
    </div>
  </form>
  </section>
</template>

<script>

export default {
  name: 'SortForm',
  components: {},
  data() {
    return {
      city: '',
    }
  },
  methods: {
  }
}
</script>

<style scoped>
.sort-form {
  display: flex;
}

.sort-form form {
  display: flex;
  min-width: 712px;
  padding: 12px 20px;

  background-color: var(--color-blue-main);
}

.sort-form__group {
  display: flex;
  flex-wrap: wrap;
  align-items: start;
  flex-shrink: 0;
  margin-right: 20px;
  margin-bottom: -2px;
}

.sort-form__group:last-child {
  margin-right: 0;
}

.sort-form__group > div {
  margin-right: 2px;
  margin-bottom: 2px;
}

.sort-form__group > div:last-child {
  margin-right: 0;
}

.sort-form__group > div:last-child {
  margin-right: 0;
}

/* Style for inputs */
.input-wrapper {
  display: flex;
}

.input-wrapper input {
  border-radius: 2px;
}

.input-wrapper--search input {
  width: 254px;
  padding: 8px 20px;

  color: var(--color-text-input);

  background-color: var(--color-input-base);
  border: none;
  outline: none;

  transition: background-color var(--transition-base);
}

.input-wrapper--search input:hover {
  background-color: var(--color-input-hover);
}

.input-wrapper--search input:focus::placeholder {
  opacity: 0;
}

.input-wrapper--search input:focus::-ms-input-placeholder {
  opacity: 0;
}

.input-wrapper--search input:focus {
  background-color: var(--color-input-focus);
}

.input-wrapper--search input::placeholder {
  color: var(--color-text-placeholder);

  transition: opacity var(--transition-base);
}

.input-wrapper--search input::-ms-input-placeholder {
  color: var(--color-text-placeholder);

  transition: opacity var(--transition-base);
}

.input-wrapper--radio label,
.input-wrapper--checkbox label {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 40px;
  height: 40px;

  background-color: var(--color-label-base);
  border-radius: 2px;
  cursor: pointer;

  transition: background-color var(--transition-base),
  box-shadow var(--transition-base);

  user-select: none;
}

.input-wrapper--radio label {
  justify-content: space-between;
  padding: 10px;
}

.input-wrapper--radio label:hover,
.input-wrapper--checkbox label:hover {
  background-color: var(--color-label-hover);
  box-shadow: 0 4px 10px rgba(11, 23, 78, 0.5);
}

.input-wrapper--radio label:active,
.input-wrapper--checkbox label:active {
  background-color: var(--color-label-active);
}

.input-wrapper--radio label > span,
.input-wrapper--checkbox label > span {
  transition: opacity var(--transition-base);
}

.input-wrapper--radio label:active > span,
.input-wrapper--checkbox label:active > span {
  opacity: 0.3;
}

.input-wrapper--radio input,
.input-wrapper--checkbox input {
  position: absolute;

  width: 1px;
  height: 1px;
  margin: -1px;

  clip: rect(0 0 0 0);
}

.input-wrapper--radio input:focus + label,
.input-wrapper--checkbox input:focus + label {
  background-color: var(--color-label-hover);
}

.input-wrapper--radio input:disabled + label,
.input-wrapper--checkbox input:disabled + label {
  opacity: 0.5;

  pointer-events: none;
}

.input-wrapper--radio input:checked + label,
.input-wrapper--checkbox input:checked + label {
  background-color: var(--color-label-active);
  box-shadow: none;
}

.input-wrapper--radio input:checked + label:hover,
.input-wrapper--checkbox input:checked + label:hover {
  background-color: var(--color-label-hover-checked);
}

.input-wrapper--radio input:checked:focus + label,
.input-wrapper--checkbox input:checked:focus + label {
  background-color: var(--color-label-hover-checked);
}



/* Style for icons */

.icon {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-shrink: 0;
  width: 24px;
  height: 24px;

  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
}

.icon--arrow-down {
  width: 20px;
  height: 22px;

  /*background-image: url("../../img/icon/icon-arrow-down.svg");*/
  background-image: url("../assets/icon/icon-arrow-down.svg");
}

.icon--arrow-up {
  width: 20px;
  height: 22px;

  background-image: url("../assets/icon/icon-arrow-up.svg");
}

.icon--strips-small {
  width: 6px;
  height: 16px;

  background-image: url("../assets/icon/icon-strips-small.svg");
}

.icon--strips-big {
  width: 6px;
  height: 22px;

  background-image: url("../assets/icon/icon-strips-big.svg");
}

.icon--rainy {
  background-image: url("../assets/icon/icon-rainy.svg");
}

.icon--sunny {
  background-image: url("../assets/icon/icon-sunny.svg");
}

.icon--cloudy {
  background-image: url("../assets/icon/icon-cloudy.svg");
}

.icon--snowy {
  background-image: url("../assets/icon/icon-snowy.svg");
}

.icon--stormy {
  background-image: url("../assets/icon/icon-stormy.svg");
}

.icon--blizzard {
  background-image: url("../assets/icon/icon-blizzard.svg");
}

.icon--metorite {
  background-image: url("../assets/icon/icon-metorite.svg");
}

.icon--wind {
  background-image: url("../assets/icon/icon-wind.svg");
}


</style>
