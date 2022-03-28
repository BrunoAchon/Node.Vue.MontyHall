<template>
    <div class="door-area">
        <div class="door-frame" :class="{ selected: selected && !open }">
            <Gift v-if="open && hasGift"/>
        </div>
        <div class="door"  :class="{ open }"
            @click="selected =!selected">
            <div class="number" :class="{ selected }">{{number}}</div>
            <div class="knob" :class="{ selected }"
                @click="open = true"></div>
        </div>
    </div>
</template>

<script>
import Gift from './Gift'

export default {
    name:'door-hall',
    components: { Gift },
    props: {
        number:{},
        hasGift: { type: Boolean }
    },
    data: function(){
        return{
            open: false,
            selected: false
        }
    }
}
</script>

<style>
:root{
    --door-border: 5px solid brown;
    --selected-border: 5px solid yellow;
    --selected-color: yellow;
    --selected-bg: yellow;
}

.door-area{
    border-bottom: 10px solid #aaa;
    display: flex;
    font-size: 3rem;
    height: 310px;
    justify-content: center;
    margin-bottom: 20px;
    position: relative;
    width: 200px;
}

.door-frame{
    align-items: flex-end;
    border-left: var(--door-border);
    border-right: var(--door-border);
    border-top: var(--door-border);
    display: flex;
    height: 300px;
    justify-content: center;
    position: absolute;
    width: 180px;
}

.door{
    align-items: center;
    background-color: chocolate;
    display: flex;
    flex-direction: column;
    height: 295px;
    padding: 20px;
    position: absolute;
    top: 5px;
    width: 170px;
}

.door .knob{
    align-self: flex-start;
    background-color: brown;
    border-radius: 10px;
    height: 20px;
    margin-top: 60px;
    width: 20px;
}

.door-frame.selected{
    border-left: var(--selected-border);
    border-right: var(--selected-border);
    border-top: var(--selected-border);
}

.door .number.selected{
    color: var(--selected-color);
}

.door .knob.selected{
    background-color: var(--selected-bg);
}

.door.open {
    background-color: #0007;
}

.door.open .knob{
    display: none;
}

.door.open .number{
    display: none;
}

</style>