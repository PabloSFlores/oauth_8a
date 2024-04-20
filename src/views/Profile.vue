<template>
    <div>
        <b-card title="Información del usuario" class="my-5 mx-5">
            <b-row>
                <b-col sm="2">
                    <b-img v-bind="mainProps" rounded fluid :src="$auth.user.picture"></b-img>
                </b-col>
                <b-col sm="10">
                    <b-card-body>
                        <b-card-text>
                            <h2>{{ $auth.user.name }}</h2>
                            <p>{{ $auth.user.email }}</p>
                        </b-card-text>
                    </b-card-body>
                </b-col>
            </b-row>
        </b-card>
        <div>
            <pre>{{ JSON.stringify($auth.user, null, 2) }}</pre>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            mainProps: {
                width: 150,
                height: 100,
                class: 'my-2 mx-2'
            }
        }
    }
}
</script>
