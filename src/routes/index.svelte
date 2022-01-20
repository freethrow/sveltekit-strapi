<script context="module">

    export async function load({fetch}){

        const res = await fetch('https://ft-strapi-reviews.herokuapp.com/api/articles?populate=*')

        const jsonRes = await res.json()
        console.log(jsonRes.data)
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



<div>
    <h1>SvelteKit + Strapi News ooh</h1>
</div>



