<script lang="ts">
	import { onMount } from "svelte";
	import { random } from "gsap/gsap-core";

    let { shape, color, animation, size, className} : { shape: string, color: string, animation: string, size: number, className: string} = $props();

    let ctx : gsap.Context;
    
    onMount(() => {
        ctx = gsap.context(() => {
            gsap.fromTo(
                '.updown',
                {
                    yPercent: 50,
                    // choose any value between -50 and 50
                    xPercent: random(-50, 50, 50)
                },
                {
                    yPercent: 0,
                    xPercent: 0,
                    duration: 3,
                    repeat: -1,
                    yoyo: true,
                    ease: 'power1'
                }
            )

            gsap.fromTo(
                '.rotate',
                {
                    rotate: (i) => random(-360, 360, 50),
                },
                {
                    rotate: 0,
                    duration: 5,
                    repeat: -1,
                    ease: 'power1',
                    yoyo: true,
                    stagger: 0.5,

                }
            )
        })

        return () => {
            ctx.revert()
        }
    })
</script>

<div 
    class="{className} {animation} {shape === 'circle' ? 'rounded-full' : ''}" 
    style="background-color: {color}; width: {size}px; height: {size}px;"
></div>