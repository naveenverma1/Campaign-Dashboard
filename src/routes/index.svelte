
<script>
      import Breadcrumb from "sveltestrap/src/Breadcrumb.svelte";
  import BreadcrumbItem from "sveltestrap/src/BreadcrumbItem.svelte";
  import DashboardCard from "../components/DashboardCard.svelte";
  import Row from "sveltestrap/src/Row.svelte";
  import CustomCard from "../components/CustomCard.svelte";
  import Table from "../components/Table.svelte";
 export let cardTitle="Campaigns Data "
 import AreaChart from "../components/Charts/AreaChart.svelte";
 import BarChart from "../components/Charts/BarChart.svelte";

import Layout from "../components/layout.svelte"

let title = "Campaign Dashboard";



</script>


<svelte:head>
  <title>{title}</title>
</svelte:head>
<Layout>

<h1 class="mt-4">Dashboard</h1>

<Breadcrumb class="mb-4">
    <BreadcrumbItem active>Dashboard</BreadcrumbItem>
  </Breadcrumb>
<h1>{title}</h1>

<Row>
    <div class="col-xl-3 col-md-6">
      <DashboardCard cardTitle="affle" cardColor="primary" />
    </div>
    <div class="col-xl-3 col-md-6">
        <DashboardCard cardTitle="appnext" cardColor="warning" />
      </div>
      <div class="col-xl-3 col-md-6">
        <DashboardCard cardTitle="inmobi" cardColor="success" />
      </div>
      <div class="col-xl-3 col-md-6">
        <DashboardCard cardTitle="globale" cardColor="danger" />
      </div>
</Row> 
<!-- <div class="col-xl-6">
<Layout>
  
</Layout>
</div> -->
<Row>
    <div class="col-xl-6">
      <CustomCard cardTitle="Area Chart Example" cardIcon="fas fa-chart-area">
        <AreaChart />
      </CustomCard>
    </div>
    <div class="col-xl-6">
      <CustomCard cardTitle="Bar Chart Example" cardIcon="fas fa-chart-bar">
        <BarChart />
      </CustomCard>
    </div>
  </Row>
<CustomCard cardTitle="{cardTitle}" cardIcon="fas fa-table">
    <Table />
  </CustomCard>

</Layout>