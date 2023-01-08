<template>
    <div>
        <ul class="list-group">
            <li class="list-group-item">
               Server #{{ serverData.id }}
               <p> Durumu : <strong> {{ serverData.status }}</strong></p>
            </li>      
        </ul>
    </div>
</template>
<!-- props dıştan içe, yani component'i kapsayan alandan component'e ve sub-component'e doğru aktalırı
(one way down binding)-->
<script>
    export default {
        props : ["serverData"] 
    }
</script>