<script lang="ts">
    import { PrivateKey } from '@bsv/sdk'
    
    let WIF:string
    let address:string
    
    function createKeys () {
    
        const privKey = PrivateKey.fromRandom()
        WIF = privKey.toWif()
        console.log("Private Key WIF format is ", WIF)
        address = privKey.toAddress()
        console.log("Your bitcoin address is ", address)
    }
    
    </script>
    
    <div class="flex flex-col items-center mt-6">
        <button class="mt-6 bg-black text-white p-2 rounded mx-auto outline outline-offset-2 outline-blue-500 ..." on:click={createKeys}> Generate New Wallet Keys </button>
        <p class="mt-6">Private Key WIF format is : {WIF}</p>
        <p class="mt-6">Your BitCoin Address is : {address}</p>
    </div>
    

    
    