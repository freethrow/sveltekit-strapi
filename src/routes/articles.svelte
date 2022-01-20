<script context="module">

    export async function load({fetch}){

        const res = await fetch('https://ft-strapi-reviews.herokuapp.com/api/articles?populate=*')

        const jsonRes = await res.json()
    
        return {
            props:{
                articles: jsonRes.data
            }
            
        }

       
    }

</script>

<script>
    export let articles
</script>



<h1 class="">News</h1>

<div class="grid grid-cols-1 gap-5 md:grid-cols-2">
    {#each articles as article}
        <div class="shadow-lg">
            
            <img class=" opacity-50 hover:opacity-100 transition duration-1000" src="{article.attributes.cover.data.attributes.url}" alt="{article.attributes.cover.data.attributes.name}">
            <div class="p-5">
            <h2 class="text-pink-700 font-semibold text-center">{article.attributes.title}</h2>
            <div>{article.attributes.body}</div>
        </div>
        </div>

    {/each}
</div>



