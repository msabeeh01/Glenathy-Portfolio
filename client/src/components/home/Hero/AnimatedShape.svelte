<script lang="ts">
	import { onMount } from "svelte";
    import {gsap} from 'gsap';

    let { shape, color, animation, size, className} : { shape: string, color: string, animation: string, size: number, className: string} = $props();

    let ctx : gsap.Context;
    
    onMount(() => {
        ctx = gsap.context(() => {
            gsap.fromTo(
                '.updown',
                {
                    yPercent: 100,
                },
                {
                    yPercent: 0,
                    duration: 2,
                    repeat: -1,
                    yoyo: true,
                    ease: 'power2.inOut'
                }
            )

            gsap.fromTo(
                '.rotate',
                {
                    rotate: 360,
                },
                {
                    rotate: 0,
                    duration: 4,
                    repeat: -1,
                    ease: 'power1'
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