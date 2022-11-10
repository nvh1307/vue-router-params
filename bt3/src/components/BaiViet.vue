
<template>
  <div>
      <div v-for="item in baiViets" :key="item.id">
         <router-link :to="`chitietbaiviet/${item.id}`">
            <h1>{{item.nguoiTao}}</h1>
            <p>{{item.noiDung}}</p>
            <img :src="item.linkAnh" alt="">
         </router-link>
         
      </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      baiViets: [
        {
          id: 1,
          linkAnh: "https://www.dungplus.com/wp-content/uploads/2019/12/girl-xinh-1-480x600.jpg",
          noiDung: "Some example text some example text. John Doe is an architect and engineer",
          nguoiTao: "Quoc",
        },
        {
          id: 2,
          linkAnh: "https://i.pinimg.com/280x280_RS/82/50/d0/8250d04e9d24487b578f7a6f50402807.jpg",
          noiDung: "Some example text some example text. John Doe is an architect and engineer",
          nguoiTao: "Quoc",
        },
        {
          id: 3,
          linkAnh: "https://ttol.vietnamnetjsc.vn//2018/03/07/21/04/nu-sinh-17-tuoi-duoc-khen-dep-thuan-khiet-nhu-thien-su_11.jpg",
          noiDung: "Some example text some example text. John Doe is an architect and engineer",
          nguoiTao: "Quoc",
        },
        {
          id: 4,
          linkAnh: "https://thuthuatnhanh.com/wp-content/uploads/2019/05/gai-xinh-toc-ngan-facebook.jpg",
          noiDung: "Some example text some example text. John Doe is an architect and engineer",
          nguoiTao: "Quoc",
        },
        {
          id: 5,
          linkAnh: "https://i.pinimg.com/736x/29/ab/5a/29ab5acafc429ac807f72aece29a5695.jpg",
          noiDung: "Some example text some example text. John Doe is an architect and engineer",
          nguoiTao: "Quoc",
        },
      ],
    };
  },
};
</script>
