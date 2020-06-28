<template>
    <div id="app">
        <div class="container">
                <h4>Our Customer Listings</h4>

                <div class="card mb-2 col" v-for="customer in customers" v-bind:key="customer.id">
                    <div class="card-body">
                        <h4 class="card-title">{{customer.email}}</h4>
                        <p class="card-text">{{customer.name}} </p>
                    </div>
                </div>        
         </div>   
    </div>    
</template>

<script>
export default {
    data() {
        return {
            customers: []
        }
    },
    created() {
        this.getCustomers();
    },
    methods: {
        getCustomers:function() {
            axios.get('https://jsonplaceholder.typicode.com/users')
                .then((response) => {
                    //console.log(response.data);
                    this.customers = response.data;
                })
                .catch((error) => {
                    console.log(error);
                })
                .then(() => {

                });
                
        }
    }

}
</script>