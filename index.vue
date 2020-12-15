<template>
    <div
        :class="`icon-${name}`"
        v-html="svg"
    />
</template>

<script>
    export default {
        props:{
            icons: {
                type: Object,
                default: {}
            },
            name: {
                type: String,
                default: 'star'
            },
            fill: {
                type: String,
                default: "#333"
            },
            width: {
                type: String,
                default: "20px"
            },
            height: {
                type: String,
                default: "20px"
            },
            rotate:{
                type: String,
                default: "0deg"
            },
            viewBox:{
                type: String,
            },
        },
        computed:{
            svg(){
                if(this.icons[this.name] && /<svg/.test(this.icons[this.name])){
                    let svg = document.createElement('svg')
                        svg.innerHTML = this.icons[this.name]
                        svg = svg.children[0]
                        svg.setAttribute('width',this.width)
                        svg.setAttribute('height',this.height)
                        svg.setAttribute('fill',this.fill)
                        svg.setAttribute('style',`transform: rotate(${this.rotate})`)
                        if(this.viewBox) svg.setAttribute('viewBox',this.viewBox)
                        
                        if(this.fill) svg.querySelectorAll('path, rect, circle').forEach(g=>{
                            g.style.fill = this.fill
                        })
                    return svg.outerHTML
                } else {
                    console.warn(`"${this.name}" icon couldn't found!`)
                    return `<b style="font-size:10px;color: red">"${this.name}" icon not found!</b>`
                }
            }
        },
    }
</script>