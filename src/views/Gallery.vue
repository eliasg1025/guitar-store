<template>
  <Layout
    bannerImgName="gallery/banner-gallery"
    bannerText="Lorem ipsum dolor sit amet"
  >
    <Modal ref="modal">
      <img :src="modalImg" alt="" class="modal__img" id="modal__img" />
    </Modal>

    <main class="main">
      <div class="group gallery">
        <h2 class="group__title">Nuestra Galeria</h2>
        <div class="container container--flex">
          <div class="column column--50-25">
            <img
              @click="openModal"
              src="@/assets/img/gallery/gallery1.jpeg"
              alt=""
              class="gallery__img gallery__img--big"
            />
            <img
              @click="openModal"
              src="@/assets/img/gallery/gallery2.jpeg"
              alt=""
              class="gallery__img gallery__img--small"
            />
          </div>
          <div class="column column--50-25">
            <img
              @click="openModal"
              src="@/assets/img/gallery/gallery3.jpeg"
              alt=""
              class="gallery__img gallery__img--small"
            />
            <img
              @click="openModal"
              src="@/assets/img/gallery/gallery4.jpeg"
              alt=""
              class="gallery__img gallery__img--big"
            />
          </div>
          <div class="column column--50-25">
            <img
              @click="openModal"
              src="@/assets/img/gallery/gallery5.jpeg"
              alt=""
              class="gallery__img gallery__img--big"
            />
            <img
              @click="openModal"
              src="@/assets/img/gallery/gallery6.jpeg"
              alt=""
              class="gallery__img gallery__img--small"
            />
          </div>
          <div class="column column--50-25">
            <img
              @click="openModal"
              src="@/assets/img/gallery/gallery7.jpeg"
              alt=""
              class="gallery__img gallery__img--small"
            />
            <img
              @click="openModal"
              src="@/assets/img/gallery/gallery8.jpeg"
              alt=""
              class="gallery__img gallery__img--big"
            />
          </div>
        </div>
      </div>
    </main>
  </Layout>
</template>

<script>
  import Layout from '@/components/layout/Layout';
  import Modal from '@/components/shared/Modal';

  export default {
    name: 'Gallery',
    components: {
      Layout,
      Modal
    },
    data() {
      return {
        modalImg: ''
      };
    },
    methods: {
      openModal(evt) {
        this.modalImg = evt.toElement.src;
        this.$refs.modal.openModal();
      }
    }
  };
</script>

<style lang="scss" scoped>
  .gallery__img {
    object-fit: cover;
    margin-bottom: 10px;
    cursor: pointer;
    transition: all 0.5s;
  }
  .gallery__img:hover {
    transform: scale(1.02);
  }
  .gallery__img--big {
    height: 400px;
  }
  .gallery__img--small {
    height: 200px;
  }
  .modal__img {
    width: 70%;
  }
</style>
