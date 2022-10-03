<template>
  <div name="modal">
    <div class="modal-mask">
      <div class="modal-wrapper">
        <div class="modal-container">
          <div class="modal-body">
            <p class="title">
              El usuario <span>{{ $route.params.id }}</span> no existe, por
              favor introduce otro usuario.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'userNotFound',
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
span {
  color: red;
}
.modal-container {
  width: 600px;
  height: 200px;
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
    height: 200px;
  }
  .title {
    margin: 50px;
    line-height: 25px;
  }
}

@media screen and (max-width: 400px) {
  .modal-container {
    width: 150px;
    height: 100px;
  }
  .title {
    margin: 10px 0px 0px 0px;
    font-size: 0.8rem;
  }
}
</style>
