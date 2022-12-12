<style>
hr {
  /* margin-top: 0.5rem;
  margin-bottom: 0.5rem; */
  border: 0;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
}

.user-avatar {
  width: 15em;
  height: 15em;
}

.user-avatar>span>i {
  font-size: 15em;
  color: rgb(220, 236, 241);

}

.p-details>li,
.p-docs>li {
  height: 2.3em;
}

.p-details>li {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  padding: 0 0 0 4px;
  font-weight: bolder;
  font-size: small;
  color: black;

}

.p-docs>li {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 6px 0 6px;
  font-weight: lighter;
}

.p-docs>li a {
  color: rgb(20, 20, 228);
}

.p-docs>li a:hover {
  color: rgb(9, 89, 113);
}

.progress,
.p-details>li:nth-child(odd),
.p-docs>li:nth-child(odd) {
  background-color: rgb(220, 236, 241);
}

.choose-file {
  border: 1px solid rgba(0, 0, 0, 0.1);
}

.p-icon {
  font-size: 25px;
}

/* .docs-title{
  
} */
</style>
<script>
import PageHeader from "@/components/page-header";
import Layout from "../../layouts/main";

/*Form for profile*/
export default {
  components: {
    PageHeader,
    Layout,
  },
  data() {
    return {
      title: 'Dashboard',
      items: [
        {
          text: 'Africana',
        },
        {
          text: 'User Profile',
          active: true
        },

      ],
      labelData: [
        {
          firstname: 'Sencer',
          lastname: '',
          gender: '',
          dob: '',
          idnum: '',
          maritalstate: '',
          pin: '',
          phone: '',
          email: '',
          residence: '',
          approvalstate: ''

        }
      ]
    };
  }
};
</script>

<template>
  <Layout>
    <div class="main-container">
      <PageHeader :title="title" :items="items" />
      <hr>
      <h6 class="font-size-13 font-weight-light">Your profile is 1 step away to completeness</h6>
      <div class="progress" style="height: 20px;">
        <div class="progress-bar progress-bar-striped progress-bar-animated" role="progressbar"
          aria-label="Default striped example" style="width: 20%;" aria-valuenow="20" aria-valuemin="0"
          aria-valuemax="100">20% complete</div>
      </div>
      <div class="row no-gutters">
        <div class="col-lg-6">
          <!-- Container for personal details section-->
          <div class="pr-3">
            <div class="d-flex align-items-center justify-content-center mt-4 pt-2 mr-3">
              <h4 class="text-capitalize font-weight-light pl-2 d-flex align-items-center justify-content-center "><span
                  class=""><i class="ri-account-pin-circle-line p-icon"></i></span>Personal details</h4>
            </div>
            <hr class="">
            <!-- Personal details -->
            <div class="">
              <ul class="list-unstyled p-details">
                <li class=""><span class="text-uppercase ">fisrt name:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">lastname:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">gender:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">date of birth:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">id Number:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">marital status:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">kra pin #:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">phone number:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">email address:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">residence:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">approval status:</span><label for=""></label></li>
              </ul>
            </div>
            <!-- Employment and Income section -->
            <div class="d-flex align-items-center justify-content-center  pt-2">
              <h4 class="text-capitalize font-weight-light pl-2 d-flex align-items-center justify-content-center"><span
                  class=""><i class="ri-briefcase-line p-icon"></i></span>employment and income</h4>
            </div>
            <hr class="pr-3">
            <!-- Employment & Income range details-->
            <div class="">
              <ul class="list-unstyled p-details">
                <li class=""><span class="text-uppercase">income range:</span><span
                    class=" text-secondary float-right font-weight-light">KES.0-KES.0</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">current occupation:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">employment status:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">income stream:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">time in current employment:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">employer:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase">employer number:</span><label for=""></label></li>
              </ul>
            </div>
          </div>
        </div>
        <!-- End column -->
        <!-- Beginning of User documents upload -->
        <div class="col-lg-6 ">
          <!-- Container for user documents section -->
          <div class="pl-3">
            <div class=" d-flex align-items-center justify-content-center mt-4 flex-wrap">
              <div class="user-avatar avatar-xl rounded-circle d-flex align-items-center justify-content-center p-0">
                <span class=""><i class="ri-user-fill"></i></span>
              </div>
            </div>
            <!--  -->
            <div class="d-flex justify-content-center align-items-center">
              <div class="d-flex justify-content-center align-items-center flex-wrap w-50">
                <h6 class="font-weight-light font-size-13">Passport Photo (JPG,JPEG,PNG) Only</h6>
                <div class="input-group choose-file p-1"><input type="file" /></div>
                <button class="btn btn-primary text-uppercase mt-2 w-100" href="#">update passport photo</button>
              </div>
            </div>
            <hr class="pl-3">
            <div class="d-flex align-items-center justify-content-center">
              <h4 class="font-weight-light text-capitalize pl-2 d-flex align-items-center justify-content-center">
                <span><i class="ri-upload-cloud-line p-icon"></i></span>KYC documents upload
              </h4>
            </div>
            <hr class="pl-3">
            <!-- Documents upload details -->
            <div class="">
              <ul class="list-unstyled p-docs">
                <li class="">
                  <span class="text-capitalize docs-title">ID card</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center">
                    <span class="text-right"><i class="ri-close-line"></i>Not uploaded</span></span>
                  <a href="#" class="link-primary">Upload now</a>
                </li>
                <li class="">
                  <span class="text-capitalize docs-title">KRA pin</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center"><i
                      class="ri-close-line"></i>Not uploaded</span>
                  <a href="#">Upload now</a>
                </li>
                <li class="">
                  <span class="text-capitalize ">spouse ID</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center"><i
                      class="ri-close-line"></i>Not uploaded</span>
                  <a href="#">Upload now</a>
                </li>
                <li class="">
                  <span class="text-capitalize docs-title">spouse KRA pin</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center"><i
                      class="ri-close-line"></i>Not uploaded</span>
                  <a href="#">Upload now</a>
                </li>
                <li class="">
                  <span class="text-capitalize docs-title">marriage certificate</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center"><i
                      class="ri-close-line"></i>Not uploaded</span>
                  <a href="#">Upload now</a>
                </li>
                <li class="">
                  <span class="text-capitalize docs-title">birth certificate</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center"><i
                      class="ri-close-line"></i>Not uploaded</span>
                  <a href="#">Upload now</a>
                </li>
                <li class="">
                  <span class="text-capitalize docs-title">divorce certificate</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center"><i
                      class="ri-close-line"></i>Not uploaded</span>
                  <a href="#">Upload now</a>
                </li>
                <li class="">
                  <span class="text-captalize docs-title">death certificate</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center"><i
                      class="ri-close-line"></i>Not uploaded</span>
                  <a href="#">Upload now</a>
                </li>
                <li class="">
                  <span class="text-capitalize docs-titles">proof of residence</span>
                  <span class="Not-uploaded w-50 d-flex align-items-center justify-content-center"><i
                      class="ri-close-line"></i>Not uploaded</span>
                  <a href="#">Upload now</a>
                </li>
              </ul>
            </div>
          </div>
          <!-- End of container for user docs -->
        </div>
        <!-- End of docs column -->
      </div>
      <!-- End row -->
      <div class="row no-gutters">
        <div class="col-lg-6">
          <!-- Family and residence section container-->
          <div class="pr-3">
            <div class="d-flex align-items-center justify-content-center mt-4 pt-2">
              <h4 class="text-capitalize font-weight-light pl-2 d-flex align-items-center justify-content-center"> <span
                  class=""><i class="ri-team-line p-icon"></i></span>Family and residence</h4>
            </div>
            <hr class="pr-3">
            <!-- family and residence details -->
            <div class="">
              <ul class="list-unstyled p-details">
                <li class=""><span class="text-uppercase">number of dependants:</span><span
                    class=" text-secondary float-right font-weight-light">KES.0-KES.0</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">current residence:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">living with family?:</span><span
                    class=" text-secondary float-right font-weight-light">NO</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">current rent amount:</span><span
                    class=" text-secondary float-right font-weight-light">00.0</span><label for=""></label></li>
              </ul>
            </div>
            <!-- Next of Kins section -->
            <div class="d-flex align-items-center justify-content-center pt-2">
              <h4 class="text-capitalize font-weight-light pl-2 d-flex align-items-center justify-content-center"><span class=""><i class="ri-user-heart-line p-icon"></i></span>next of kins</h4>
            </div>
            <hr class="pr-3">
            <div class="table-responsive">
              <table class="table">
                <thead class=" bg-primary">
                  <tr>
                    <th scope="col" class="text-light">#</th>
                    <th scope="col" class="text-uppercase text-light">name</th>
                    <th scope="col" class="text-uppercase text-light">ID number</th>
                    <th scope="col" class="text-uppercase text-light">phone</th>
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
        <div class="col-lg-6">
          <!-- Home ownership container section -->
          <div class="pl-3">
            <div class="d-flex align-items-center justify-content-center p-3">
              <h4 class="font-weight-light text-capitalize pl-2 d-flex align-items-center justify-content-center"><span><i class="ri-home-gear-line p-icon"></i></span>home ownership preferences</h4>
            </div>
            <hr class="pl-3">
            <!-- Home ownership details -->
            <div class="">
              <ul class="list-unstyled p-details">
                <li class=""><span class="text-uppercase">resaon for home ownership:</span><label for=""></label></li>
                <li class=""><span class="text-uppercase ">1<sup>st</sup> county of preference:</span><label
                    for=""></label></li>
                <li class=""><span class="text-uppercase ">2<sup>nd</sup> county of preference:</span><label
                    for=""></label></li>
                <li class=""><span class="text-uppercase ">3<sup>rd</sup> county of preference:</span><label
                    for=""></label></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <!-- End row of Family residence & home preference -->
      <div class="d-flex justify-content-end p-2">
        <a class="btn btn-primary w-25" href="">Edit profile</a>
      </div>
      <hr>
    </div>
    <!-- End of the main-container -->
  </Layout>
</template>