<script>
  // components for this layout
  import AdminNavbar from "../_components/Navbars/AdminNavbar.svelte";
  import Sidebar from "../_components/Sidebar/Sidebar.svelte";
  import HeaderStats from "../_components/Headers/HeaderStats.svelte";
  import FooterAdmin from "../_components/Footers/FooterAdmin.svelte";
</script>

<div>
  <Sidebar {location} />
  <div class="relative md:ml-64 bg-blueGray-100">
    <AdminNavbar />
    <HeaderStats />
    <div class="px-4 md:px-10 mx-auto w-full -m-24">
      <slot />
      <FooterAdmin />
    </div>
  </div>
</div>
