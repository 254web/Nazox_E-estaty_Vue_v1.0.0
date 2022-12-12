<style>
.sup-docs {
  background-color: rgba(182, 174, 174, 0.1);
  height: 5em;
}

.div-button>a {
  height: 2em;
}
</style>
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
          text: 'My Documents',
          active: true
        },

      ],
      // transactionData: [
      //   {
      //     orderid: "#NZ1563",
      //     date: "28 Mar, 2020",
      //     billingname: "Frank Dean",
      //     total: "$164",
      //     paymentstatus: "Unpaid"
      //   },
      //   {
      //     orderid: "#NZ1564",
      //     date: "28 Mar, 2020",
      //     billingname: "Eddy Torres",
      //     total: "$141",
      //     paymentstatus: "Paid"
      //   },
      //   {
      //     orderid: "#NZ1565",
      //     date: "29 Mar, 2020",
      //     billingname: "Jamison Clark",
      //     total: "$123",
      //     paymentstatus: "Paid"
      //   },
      //   {
      //     orderid: "#NZ1566",
      //     date: "30 Mar, 2020",
      //     billingname: "Jewel Buckley",
      //     total: "$112",
      //     paymentstatus: "Paid"
      //   },
      //   {
      //     orderid: "#NZ1567",
      //     date: "31 Mar, 2020",
      //     billingname: "Jeffrey Waltz",
      //     total: "$105",
      //     paymentstatus: "Unpaid"
      //   },
      //   {
      //     orderid: "#NZ1568",
      //     date: "01 Apr, 2020",
      //     billingname: "Jefferson Allen",
      //     total: "$160",
      //     paymentstatus: "Chargeback"
      //   },
      //   {
      //     orderid: "#NZ1569",
      //     date: "02 Apr, 2020",
      //     billingname: "Paul Jones",
      //     total: "$183",
      //     paymentstatus: "Paid"
      //   },
      //   {
      //     orderid: "#NZ1570",
      //     date: "03 Apr, 2020",
      //     billingname: "Donald Bailey",
      //     total: "$146",
      //     paymentstatus: "Paid"
      //   },
      //   {
      //     orderid: "#NZ1571",
      //     date: "03 Apr, 2020",
      //     billingname: "Jimmy Barker",
      //     total: "$165",
      //     paymentstatus: "Unpaid"
      //   },
      //   {
      //     orderid: "#NZ1572",
      //     date: "04 Apr, 2020",
      //     billingname: "Walter Brown",
      //     total: "$172",
      //     paymentstatus: "Paid"
      //   }
      // ],
      // totalRows: 1,
      // currentPage: 1,
      // perPage: 5,
      // pageOptions: [5, 10, 25, 50],
      // filter: null,
      // filterOn: [],
      // sortBy: "orderid",
      // sortDesc: false,
      // fields: [
      //   { key: "orderid", sortable: true, label: "Order ID" },
      //   { key: "date", sortable: true },
      //   { key: "billingname", sortable: true, label: "Billing Name" },
      //   { key: "total", sortable: true, label: "Total" },
      //   { key: "paymentstatus", sortable: true, label: "Payment Status" },
      //   { key: "action" }
      // ]

    }
  }
}
</script>
<template>
  <Layout>
    <div class="main-container">
      <PageHeader :title="title" :items="items" />
      <div class="row no-gutters ">
        <div class="col-12">
          <div class="d-flex align-items-center justify-content-between sup-docs">
            <div class="">
              <h5 class="font-weight-bold d-flex align-items-center justify-content-center">
              <span class="font-size-24">
                <i class="ri-file-list-line"></i>
              </span> My supporting documents</h5>
            </div>

            <div class="div-button">
              <a class="btn text-uppercase btn-primary btn-upload mr-1 d-flex align-items-center justify-content-center"
                href="#">
                <span><i class="ri-add-circle-line"></i></span>upload document</a>
            </div>
            <!-- App Search-->
          </div>
          <div class="mt-2">
            <!-- <h4 class="card-title mb-4">Latest Transactions</h4> -->
            <div class="row mt-4">
              <div class="col-sm-12 col-md-6">
                <div id="tickets-table_length" class="dataTables_length">
                  <label class="d-inline-flex align-items-center">
                    Show&nbsp;
                    <b-form-select v-model="perPage" size="sm" :options="pageOptions"></b-form-select>&nbsp;entries
                  </label>
                </div>
              </div>
              <!-- Search -->
              <div class="col-sm-12 col-md-6">
                <div id="tickets-table_filter" class="dataTables_filter text-md-right">
                  <label class="d-inline-flex align-items-center">
                    Search:
                    <b-form-input v-model="filter" type="search"
                      class="form-control form-control-sm ml-2"></b-form-input>
                  </label>
                </div>
              </div>
              <!-- End search -->
            </div>
            <div class="table-responsive">
              <!-- <b-table class="" :items="transactionData" :fields="fields" responsive="sm" :per-page="perPage"
                :current-page="currentPage" :sort-by.sync="sortBy" :sort-desc.sync="sortDesc" :filter="filter"
                :filter-included-fields="filterOn" @filtered="onFiltered">
                <template v-slot:cell(paymentstatus)="row">
                  <div class="badge font-size-12" :class="{
                    'badge-soft-danger': `${row.value}` === 'Chargeback',
                    'badge-soft-success': `${row.value}` === 'Paid',
                    'badge-soft-warning': `${row.value}` === 'Unpaid'
                  }">{{ row.value }}</div>
                </template>

                <template v-slot:cell(action)>
                  <a href="javascript:void(0);" class="mr-3 text-primary" v-b-tooltip.hover data-toggle="tooltip"
                    title="Edit">
                    <i class="mdi mdi-pencil font-size-18"></i>
                  </a>
                  <a href="javascript:void(0);" class="text-danger" v-b-tooltip.hover title="Delete">
                    <i class="mdi mdi-trash-can font-size-18"></i>
                  </a>
                </template>
              </b-table> -->
              <!--  -->
              <table class="table">
                <thead class=" bg-primary">
                  <tr>
                    <th scope="col" class="text-light">#</th>
                    <th scope="col" class="text-uppercase text-light" :per-page="perPage">document type</th>
                    <th scope="col" class="text-uppercase text-light">document url</th>
                    <th scope="col" class="text-uppercase text-light"></th>
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
          <div class="row">
            <div class="col">
              <div class="font-size-13 font-weight-light">
                <h6 class="font-size-13 font-weight-light">showing 0 to 0 of 0 entries</h6>
              </div>
            </div>
            <div class="col">
              <div class="dataTables_paginate paging_simple_numbers float-right">
                <ul class="pagination pagination-rounded mb-0">
                  <!-- pagination -->
                  <b-pagination v-model="currentPage" :total-rows="rows" :per-page="perPage"></b-pagination>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Layout>
</template>