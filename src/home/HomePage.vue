<template>
    <div class="hello-world" style="margin-top: 8rem;">
        {{ helloWorld }}
    </div>
</template>

<script>
export default {
    name: "HomePage",

    data() {
        return {
            helloWorld: null
        };
    },

    async created() {
        const requestBody = {
            hello: "world"
        };

        let response = await this.getAdminHelloWorld(requestBody);
        console.log(response);
        this.helloWorld = response.body;
    },

    methods: {
        async getAdminHelloWorld(requestBody) {
            let URL = "/api/v1/admin/hello-world";

            const res = await fetch(URL, {
                method: "POST",
                headers: {
                    "Content-Type": "application/json"
                },
                body: JSON.stringify(requestBody)
            });

            const data = await res.json();

            return {
                status: res.status,
                body: data
            };
        }
    }
}
</script>
