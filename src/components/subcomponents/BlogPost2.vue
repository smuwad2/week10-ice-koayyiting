<script>
    export default {
        // Add code if/as necessary
        // Hint: Add properties subject, entry and mood
        props: {
            id: Number,
            subject: String,
            entry: String,
            mood: String
        },
        computed: {
            imageSrc() {
                return `/assets/${this.mood}.png`
            }
        }
    }
</script>


<template>
    <!-- TODO: add your template code here Use boostrap card --> 
    <div class="card mb-3" style="width: 18rem;">
        <img :src="imageSrc" class="card-img-top" alt="Mood Image">
        <div class="card-body">
            <h5 class="card-title">{{ subject }}</h5>
            <p class="card-text">{{ entry }}</p>

            <slot></slot>
        </div>
    </div>
</template>

