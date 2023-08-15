<template>
    <div class="mb-3">
        <form action="">
            <div class="mb-3">
                <label for="">Page Title</label>
                <input type="text" v-model="pageTitle" />
            </div>
            <div class="mb-3">
                <label for="">Content</label>
                <textarea rows="5" v-model="pageContent"></textarea>
            </div>
            <div class="mb-3">
                <button @click.prevent="submitForm">
                    Create Page
                </button>
            </div>
        </form>
    </div>
</template>


<script>

export default {
    props: ["pageCreated"],

    data() {
        return {
            pageTitle: "",
            pageContent: ""
        }
    },

    methods: {
        submitForm() {
            if (!this.pageTitle || !this.pageContent) {
                alert("Please Fill The Form!");
                return;
            }

            this.pageCreated({
                pageTitle: this.pageTitle,
                pageContent: this.pageContent
            })
        }
    }
}
</script>
