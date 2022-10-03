<template>
  <div name="modal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-body">
            <p class="title">
              ¡Muchas gracias
              <span class="title-span">{{ user.data.name }}</span
              >!
            </p>
            <p class="title-email">
              Te hemos enviado un email a
              <span class="title-span">{{ user.data.email }}</span> con los
              datos de tu préstamo:
            </p>
            <p class="title-data">
              Nombre: <span class="title-span">{{ user.data.name }}</span>
            </p>
            <p class="title-data">
              Apellidos: <span class="title-span">{{ user.data.surname }}</span>
            </p>
            <p class="title-data">
              Email: <span class="title-span">{{ user.data.email }}</span>
            </p>
            <p class="title-data">
              Teléfono: <span class="title-span">{{ user.data.phone }}</span>
            </p>
            <p class="title-data">
              Edad: <span class="title-span">{{ user.data.age }}</span>
            </p>
            <p class="title-data">
              Importe:
              <span class="title-span">{{ user.data.loan_amount }} €</span>
            </p>
            <p class="title-data">
              Plazo:
              <span class="title-span">{{ user.data.loan_weeks }} año(s)</span>
            </p>
            <p class="title-soon">Pronto nos pondremos en contacto contigo.</p>
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
  name: 'userCorrectData',
  props: {
    show: Boolean,
    user: Object,
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
  font-size: 24px;
  display: table-cell;
  vertical-align: middle;
}

.title {
  text-align: center;
  margin: 30px;
}
.title-email {
  text-align: center;
  margin: 30px;
  line-height: 25px;
}
.title-data {
  text-align: center;
  margin: 15px;
  color: black;
}
.title-span {
  font-weight: bold;
  color: var(--gold);
}
.title-soon {
  text-align: center;
  font-weight: bold;
  margin: 30px;
}
.modal-footer {
  text-align: center;
  margin: 50px 20px 20px 20px;
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
  font-size: 18px;
}
.footer-btn:hover {
  background-color: var(--font-gray-color);
  border: 1px solid var(--gold);
}
.modal-container {
  width: 800px;
  height: 600px;
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
    width: 450px;
    height: 550px;
  }
  .title {
    margin: 20px 0px 0px 0px;
    font-size: 1.5rem;
  }
  .title-email {
    margin: 20px 0px 20px 0px;
    line-height: 25px;
    font-size: 1.5rem;
  }
  .title-data {
    margin: 10px 0px 0px 0px;
    font-size: 1.5rem;
  }

  .title-soon {
    margin: 20px 0px 0px 0px;
    font-size: 1.5rem;
  }
  .modal-footer {
    text-align: center;
    margin: 50px 0px 0px 0px;
  }
  .footer-btn {
    font-size: 1rem;
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
  .title-email {
    margin: 10px 0px 10px 0px;
    line-height: 15px;
    font-size: 0.8rem;
  }
  .title-data {
    margin: 5px 0px 0px 0px;
    font-size: 0.8rem;
  }

  .title-soon {
    margin: 10px 0px 0px 0px;
    font-size: 0.8rem;
  }
  .modal-footer {
    text-align: center;
    margin: 30px 0px 0px 0px;
  }
  .footer-btn {
    font-size: 13px;
  }
}
</style>
