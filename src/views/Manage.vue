<template>
  <div>
    <b-container fluid>
      <b-row>
        <b-col md="12" class="header-title">
          <div class="list" v-b-toggle.sidebar>
            <b-icon icon="list" style="width: 26px; height: 26px"></b-icon>
          </div>
          <div class="title">
            <p>manage</p>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <Sidebar />
    <b-container fluid style="padding-left: 0; padding-right: 0">
      <b-row class="main">
        <b-col md="12">
          <div class="my-5" sm="12" cols="12">
            <b-container>
              <b-card no-body>
                <b-tabs pills card>
                  <b-tab title="Product" active style="font-size: 1rem">
                    <TbProduct />
                  </b-tab>
                  <b-tab title="Category" style="font-size: 1rem">
                    <TbCategory />
                  </b-tab>
                </b-tabs>
              </b-card>
            </b-container>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Sidebar from '../components/_module/Sidebar'
import TbProduct from '../components/_module/TbProduct'
import TbCategory from '../components/_module/TbCategory'

export default {
  title: 'Data Management - GI POS',
  name: 'manage',
  components: {
    Sidebar,
    TbProduct,
    TbCategory
  }
}
</script>

<style scoped>
.header-title {
  font-size: 1.5rem;
  padding-left: 0;
  padding-right: 0;
  background: #ffffff;
  box-shadow: 0px 4px 1px rgba(0, 0, 0, 0.25);
  display: flex;
  flex-direction: row;
  align-content: space-between;
}

.title {
  padding: 5px;
  margin: auto;
  text-align: center;
  flex: 2;
}

.title p {
  font-size: 1rem;
  line-height: 25px;
  margin-bottom: 0;
}
/* product item */
.main {
  margin: 1px;
}

@media (max-width: 767px) {
  .main .items {
    font-size: 0.7rem;
  }
}

@media (min-width: 768px) and (max-width: 991.98px) {
  .main .items {
    font-size: 1rem;
  }
}
</style>
