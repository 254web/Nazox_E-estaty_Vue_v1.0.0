<script>
import PageHeader from "@/components/page-header";
import Layout from "../../layouts/main";

export default {
  components: {
    PageHeader,
    Layout
  },
  data(){
    return {
      title: 'Dashboard',
      items: [
        {
          text: 'Africana',
        },
        {
          text: 'My Documents',
          active: true
        },

      ],

}
  }
}
</script>
<template>
  <Layout>
    <div class="main-container">
      <PageHeader :title="title" :items="items"/>
      <div class="row no-gutters sup-docs d-flex align-items-center justify-content-center">
        <div class="col-lg-6">
          <div class="d-flex align-items-center justify-content-start ml-1 mr-4">
            <h4 class="text-uppercase font-weight-bold d-flex align-items-center justify-content-center ml-1">
              <span class="font-size-24 pr-1">
                <i class="ri-refund-fill"></i>
              </span>my reimbursement request
            </h4>
          </div>
        </div>
        <div class="col-lg-6">
          <div class="d-flex align-items-center justify-content-end div-button ml-4 mr-1 ">
            <a class="btn text-uppercase btn-success mr-1 d-flex align-items-center justify-content-center font-size-13"
              href="#"><span><i class="ri-add-circle-fill"></i></span>request refund</a>
            <!-- <a class="btn text-uppercase btn-secondary mr-1 d-flex align-items-center justify-content-center font-size-13"
              href="#"><span><i class="ri-printer-fill"></i></span>print statement</a>
            <a class="btn text-uppercase btn-primary mr-1 d-flex align-items-center justify-content-center font-size-13"
              href="#"><span><i class="ri-mail-fill"></i></span>email statement</a> -->
          </div>
        </div>
      </div>
      <div class="row no-gutters">
        <div class="col">
          <div class="table-responsive">
            <table class="table">
              <thead class=" bg-primary">
                <tr>
                  <th scope="col" class="text-light">#</th>
                  <th scope="col" class="text-uppercase text-light">date created</th>
                  <th scope="col" class="text-uppercase text-light">refund type</th>
                  <th scope="col" class="text-uppercase text-light">account balance</th>
                  <th scope="col" class="text-uppercase text-light">amount requested</th>
                  <th scope="col" class="text-uppercase text-light">status</th>
                  <th scope="col" class="text-uppercase text-light">action</th>
                  
                </tr>
              </thead>
              <tbody class="d-none">
                <tr>
                  <th scope="row">1</th>
                  <td></td>
                  <td></td>
                  <td></td>
                </tr>
                <tr>
                  <th scope="row">2</th>
                  <td></td>
                  <td></td>
                  <td></td>
                </tr>
                <tr>
                  <th scope="row">3</th>
                  <td></td>
                  <td></td>
                  <td></td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </Layout>

</template>