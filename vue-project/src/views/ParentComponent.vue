<template>
    <child-component ref="child_component"/>        
</template>
<script>
import ChildComponent from '../views/ChildComponent.vue';
export default {
    components : {ChildComponent},
    methods() {
        this.$refs.child_component.$refs.btn.click();
    }
}
</script>