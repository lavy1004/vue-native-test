<template>
    <Item :user="navigation"></Item>
</template>

<script>
import Item from '../../components/item'

export default {
    props: {
        navigation: {
        type: Object,
        }
    },
    components: {
        Item
    }
}
</script>