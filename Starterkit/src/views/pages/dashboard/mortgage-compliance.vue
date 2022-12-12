<script>
import PageHeader from "@/components/page-header";
import Layout from "../../layouts/main";

export default {
  components: {
    PageHeader,
    Layout
  },
  data() {
    return {
      title: 'Dashboard',
      items: [
        {
          text: 'Africana',
        },
        {
          text: 'Compliance',
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
      <PageHeader :title="title" :items="items" />
      <div class="row no-gutters">
        <div class="col-12">
          <div class="text-center text-uppercase bg-warning">
            <h4 class="d-flex align-items-center justify-content-center"><span><i
                  class="ri-qr-scan-2-fill mr-1"></i></span>mortgage compliance</h4>
          </div>
        </div>
        <div class="col-12">
          <!-- <div class="accordion w-100 bg-success" id="accordionCompliance">
            <div class="accordion-item">
              <h5 class="accordion-header" id="headingOne">
                <button class="accordion-button text-uppercase" type="button" data-bs-toggle="collapse"
                  data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne"><span><i
                      class="ri-arrow-down-s-line"></i></span>particulars of applicant <span><i
                      class="ri-file-zip-fill"></i></span></button>
              </h5>
              <div id="collapseOne" class="accordion-collapse collapse show" aria-labelledby="headingOne"
                data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  <strong>This is the first item's accordion body.</strong> It is shown by default, until the collapse
                  plugin adds the appropriate classes that we use to style each element. These classes control the
                  overall appearance, as well as the showing and hiding via CSS transitions. You can modify any of this
                  with custom CSS or overriding our default variables. It's also worth noting that just about any HTML
                  can go within the <code>.accordion-body</code>, though the transition does limit overflow.
                </div>
              </div>
            </div>
          </div> -->
          
        </div>
      </div>
    </div>
  </Layout>

</template>