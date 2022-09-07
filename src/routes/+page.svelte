<script>
  import QRCode from "qrcode-svg";

  let address = "http://expa.com/";

  $: svg = address ? new QRCode(address).svg() : '';
  
</script>

<div class="h-screen flex flex-col items-center justify-center space-y-10">

  <input
    type="text" bind:value={address}
    class="w-[258px] border py-2 px-3 rounded-lg shadow"
  />

  <span class="border rounded-lg overflow-hidden">
    {@html svg}
  </span>

</div>
