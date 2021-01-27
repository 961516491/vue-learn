<template>
    <div id="app">
        <svg width="100" height="200" xmlns="http://www.w3.org/2000/svg" style="position: absolute;" :style="{left: left1 + 'px', top: top1 + 'px'}">
            <!-- Created with Method Draw - http://github.com/duopixel/Method-Draw/ -->
            <g>
            <title>background</title>
            <rect fill="#ffffff" id="canvas_background" height="202" width="102" y="-1" x="-1"/>
            <g display="none" overflow="visible" y="0" x="0" height="100%" width="100%" id="canvasGrid">
            <rect fill="url(#gridpattern)" stroke-width="0" y="0" x="0" height="100%" width="100%"/>
            </g>
            </g>
            <g>
            <title>Layer 1</title>
            <ellipse ry="18.5" rx="16.5" id="svg_1" cy="57.953125" cx="45" stroke-width="1.5" stroke="#000" fill="#fff"/>
            <line stroke-linecap="null" stroke-linejoin="null" id="svg_3" y2="146.453125" x2="45.5" y1="77.453125" x1="44.5" fill-opacity="null" stroke-opacity="null" stroke-width="1.5" stroke="#000" fill="none"/>
            <line stroke-linecap="null" stroke-linejoin="null" id="svg_4" y2="197.453125" x2="21.5" y1="144.453125" x1="45.5" fill-opacity="null" stroke-opacity="null" stroke-width="1.5" stroke="#000" fill="none"/>
            <line stroke-linecap="null" stroke-linejoin="null" id="svg_5" y2="200.453125" x2="76.5" y1="143.453125" x1="46.5" fill-opacity="null" stroke-opacity="null" stroke-width="1.5" stroke="#000" fill="none"/>
            <line stroke-linecap="null" stroke-linejoin="null" id="svg_6" y2="125.453125" x2="19.5" y1="93.453125" x1="45.5" fill-opacity="null" stroke-opacity="null" stroke-width="1.5" stroke="#000" fill="none"/>
            <line stroke-linecap="null" stroke-linejoin="null" id="svg_8" y2="119.453125" x2="81.5" y1="95.453125" x1="43.5" fill-opacity="null" stroke-opacity="null" stroke-width="1.5" stroke="#000" fill="none"/>
            <path id="svg_10" d="m25.3725,54.468989l18.499998,-38.000006l18.499998,38.000006l-36.999995,0z" stroke-width="1.5" stroke="#000" fill="#B9FFCE"/>
            </g>
        </svg>
    </div>
</template>

<script>
export default {
    el: "#app",
    data() {
        return {
            left1: 0,
            top1: 0
        }
    },
    methods: {
        top() {
            this.top1 -= 5;
        },
        bottom() {
            this.top1 += 5
        },
        left() {
            this.left1 -= 5;
        },
        right() {
            this.left1 += 5;
        }
    },
    created() {
        const _this = this;
       document.addEventListener("keydown", function(e) {
            if (e.key == "a") {
                _this.left()
            }
            if (e.key == "d") {
                _this.right()
            }
            if (e.key == "w") {
                _this.top()
            }
            if (e.key == "s") {
                _this.bottom()
            }
        })
    }
}
</script>

<style>

</style>