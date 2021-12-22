<script>
  import Table from "sveltestrap/src/Table.svelte";

  const tableHeading = ["#", "campaignName", "sent", "impression"];
  const tableData = [
    { SNo: "1",campaignName: "affle", sent: "1333", impression: "99" },
    { SNo: "2", campaignName: "globale", sent: "3333", impression: "111" },
    { SNo: "3", campaignName: "appnext", sent: "232", impression: "2322" }
  ];
</script>

<Table bordered responsive>
  <thead>
    <tr>
      {#each tableHeading as heading}
        <th>{heading}</th>
      {/each}
    </tr>
  </thead>
  <tbody>

    {#each tableData as data}
      <tr>
        <th scope="row">{data.SNo}</th>
        <td>{data.campaignName}</td>
        <td>{data.sent}</td>
        <td>{data.impression}</td>
      </tr>
    {/each}
  </tbody>
</Table>
