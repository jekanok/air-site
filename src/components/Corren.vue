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
              <input class="form-check-input" type="checkbox" value id="defaultCheck1">
              <label class="form-check-label" for="defaultCheck1">Все</label>
            </div>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input class="form-check-input" type="checkbox" value id="defaultCheck2">
              <label class="form-check-label" for="defaultCheck2">Без пересадок</label>
            </div>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input class="form-check-input" type="checkbox" value id="defaultCheck3">
              <label class="form-check-label" for="defaultCheck3">1 пересадка</label>
            </div>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input class="form-check-input" type="checkbox" value id="defaultCheck4">
              <label class="form-check-label" for="defaultCheck4">2 пересадки</label>
            </div>
          </li>
          <li class="list-group-item d-flex justify-content-between align-items-center">
            <div class="form-check">
              <input class="form-check-input" type="checkbox" value id="defaultCheck5">
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
      isActiveeur: false
    };
  },
  methods: {
    moneyrub() {
      this.isActiveeur = false;
      this.isActiveusd = false;
      this.isActiverub = true;
    },
    moneyusd() {
      this.isActiveeur = false;
      this.isActiveusd = true;
      this.isActiverub = false;
    },
    moneyeur() {
      this.isActiveeur = true;
      this.isActiveusd = false;
      this.isActiverub = false;
    }
  },
  components: {}
};
</script>
