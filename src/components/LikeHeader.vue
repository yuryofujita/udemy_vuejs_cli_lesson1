<template>
<div>
    <slot name="title" :user="user" text="text">aaaa</slot>
    <slot></slot>
    <hr>
    <p>いいねの数</p>
    <slot name="number">aaaa</slot>
</div>
</template>

<script>
export default {
    // props:["headerText"]
    data() {
        return { 
            user: {
                firstName: "jack",
                lastName: "donald"
            }
        };
    }
};
</script>
