<script lang="ts">
	export let message: string;
    export let link: string; // Do you need linkName? for inner <a> tag?
    export let linkName: string;
</script>

<!-- Example Usage: <Alert link="https://lynix.ca/carroted-is-awesome" linkName="See More" type="error", msg=""/> -->

<!-- Colors for each alert -->
<!-- DEFCON: from-purple-700 to-blue-700 
     NORMAL-INFO: from-green-600 to to-blue-600
     WARNING-ERROR: from-red-600 to to-orange-600
--> 

<div class="absolute top-[80px] w-full px-4 py-1 inline-flex items-center w-full bg-gradient-to-r from-orange-700 to--700 py-5 w-full animated-gradient">
    <span class="text-white text-xl">
        <!-- Alert Message -->
        {message}

        <!-- This link will only appear if a link is passed to the component -->
        {#if link}
            <a href={link} class="hover:text-black hover:underline transition-colors font-bold"> {linkName}</a>
        {/if}
    </span>
</div>