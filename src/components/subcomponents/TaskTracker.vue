<script>
    // TODO: Complete the code
    export default { 
        data() {
            return {
                
            }
        },
        // Hint: insert properties task (Object) and idx (Number)
        props: {
            task: {
                type: Object,
                required: true
            },
            idx: {
                type: Number,
                required: true
            }
        },
        methods: {
            markDone() {
                // emit event back to parent with the index of the task
                this.$emit('done', this.idx)
            }
        }
    }
</script>

<template>
    <!-- TODO: add your template code here --> 
   <div class="card mb-3" style="width: 20rem;">
        <div class="card-body">
            <h5 class="card-title">{{ task.desc }}</h5>
            <p class="card-text">
                <strong>Deadline:</strong> {{ task.deadline }}
            </p>
            <button class="btn btn-success btn-sm" @click="markDone">Done</button>
        </div>
    </div>
</template>


