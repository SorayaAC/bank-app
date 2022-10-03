<template>
  <div name="modal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-body">
            <p class="title">
              Los datos introducidos no son correctos, por favor, vuelve a
              intentarlo.
            </p>
          </div>
          <div class="modal-footer">
            <button class="footer-btn" @click="$emit('close')">
              Volver al formulario
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'userErrorData',
  props: {
    show: Boolean,
  },
  data() {
    return {
      closeModal: false,
    };
  },
};
</script>

<style scoped>
.modal-mask {
  position: fixed;
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('../../assets/img/hero.png');
  display: table;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  transition: opacity 0.3s ease;
}

.modal-wrapper {
  display: table-cell;
  vertical-align: middle;
}

.title {
  text-align: center;
  margin: 80px;
  line-height: 25px;
}

.modal-footer {
  text-align: center;
  margin: 200px 20px 20px 20px;
}
.footer-btn {
  display: inline-block;
  border: 2px solid var(--font-gray-color);
  padding: 12px 34px;
  background-color: transparent;
  color: var(--gold);
  outline: none;
  border-radius: 5px;
  cursor: pointer;
  position: relative;
  transition: 0.5s;
  font-size: 14px;
}
.footer-btn:hover {
  background-color: var(--font-gray-color);
  border: 1px solid var(--gold);
}
.modal-container {
  width: 600px;
  height: 420px;
  margin: 0px auto;
  padding: 20px 30px;
  padding-bottom: 40px;
  background-color: #fff;
  border: 3px solid var(--gold);
  border-radius: 10px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.33);
  transition: all 0.3s ease;
}

@media screen and (max-width: 850px) {
  .modal-container {
    width: 290px;
    height: 450px;
  }
  .title {
    margin: 50px;
    line-height: 25px;
  }
}

@media screen and (max-width: 400px) {
  .modal-container {
    width: 150px;
    height: 400px;
  }
  .title {
    margin: 10px 0px 0px 0px;
    font-size: 0.8rem;
  }
  .modal-footer {
    text-align: center;
    margin: 250px 0px 0px 0px;
  }
  .footer-btn {
    font-size: 13px;
  }
}
</style>
