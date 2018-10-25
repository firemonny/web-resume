<template>
    <div>
    <i :class="skillSet.icon"></i> {{skillSet.skill}}
    <br>
    </div>
</template>
<script>
export default {
    props:["skillSet"]
}
</script>
