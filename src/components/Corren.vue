<!--
<template>
  <div class="menu">
    <span>Валюта</span>
    <div class="corren">
      <div class="btn-group w-100" role="group" aria-label="Basic example">
        <button
          type="button"
          @click="moneyrub"
          v-bind:class="{ active: isActiverub }"
          class="btn btn-secondary"
        >rub</button>
        <button
          type="button"
          @click="moneyusd"
          v-bind:class="{ active: isActiveusd }"
          class="btn btn-secondary"
        >usd</button>
        <button
          type="button"
          @click="moneyeur"
          v-bind:class="{ active: isActiveeur }"
          class="btn btn-secondary"
        >eur</button>
      </div>
    </div>
    <span>Количество пересадок</span>
    <div class="list-air">
      <div class="row">
        <ul class="list-group w-100">
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input
                class="form-check-input"
                v-model="transplant"
                type="checkbox"
                checked
                value="all"
                id="defaultCheck1"
                @click="transplants"
              >
              <label class="form-check-label" for="defaultCheck1">Все</label>
            </div>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input
                class="form-check-input"
                v-model="transplant"
                type="checkbox"
                value="nothing"
                id="defaultCheck2"
                @click="transplants"
              >
              <label class="form-check-label" for="defaultCheck2">Без пересадок</label>
            </div>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input
                class="form-check-input"
                v-model="transplant"
                type="checkbox"
                value="one"
                id="defaultCheck3"
                @click="transplants"
              >
              <label class="form-check-label" for="defaultCheck3">1 пересадка</label>
            </div>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input
                class="form-check-input"
                v-model="transplant"
                type="checkbox"
                value="two"
                id="defaultCheck4"
                @click="transplants"
              >
              <label class="form-check-label" for="defaultCheck4">2 пересадки</label>
            </div>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input
                class="form-check-input"
                v-model="transplant"
                type="checkbox"
                value="three"
                id="defaultCheck5"
                @click="transplants"
              >
              <label class="form-check-label" for="defaultCheck5">3 пересадки</label>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "corren",
  data() {
    return {
      isActiverub: true,
      isActiveusd: false,
      isActiveeur: false,
      transplant: ["all"]
    };
  },
  methods: {
    moneyrub() {
      this.isActiveeur = false;
      this.isActiveusd = false;
      this.isActiverub = true;
      this.$emit("changeCorrency", 1);
    },
    moneyusd() {
      this.isActiveeur = false;
      this.isActiveusd = true;
      this.isActiverub = false;
      this.$emit("changeCorrency", 58);
    },
    moneyeur() {
      this.isActiveeur = true;
      this.isActiveusd = false;
      this.isActiverub = false;
      this.$emit("changeCorrency", 65);
    },
    transplants() {
      this.$emit("transplants", this.transplant);
    }
  },
  components: {}
};
</script>
-->