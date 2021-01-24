<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Example Component</div>

                    <div class="card-body">
                        I'm an example component.
                        counter: <button v-on:click = "add">Add 1</button>
                        <p> {{counter}} </p>
                        <p v-if="counter>5" > Es mayor a 5 </p>
                    </div>
                    <div>
                        <ul>
                            <li v-for="(number,index) in collection" :key="index" >
                                {{index}}
                            </li>
                        </ul>
                    </div>    

                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        mounted() {
            console.log('Component mounted.')
        },
        data(){
            return{
                counter: 0,
                collection: [0,1,2,3] 
            }
        },
        methods:{
            add(){
                this.counter++
            }

        }
    }
</script>
