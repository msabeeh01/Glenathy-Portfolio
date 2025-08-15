<script lang="ts">
	import type { Snippet } from 'svelte';
    import styles from './typography.module.css'
  // Define a type for the allowed HTML elements
  type ElementType = 'h1' | 'h2' | 'h3' | 'p' | 'span';

  // Define a type for the visual styles of the text
  type TextType = 'heading' | 'subheading' | 'paragraph' | 'caption';

  // Define the component's props with explicit types
  interface Props {
    type?: TextType;
    class?: string;
    children?: Snippet;
    as?: ElementType; // Use the ElementType here
  }

  // Use $props() to define the component's props with default values
  let { children, type = "paragraph", class: className, as = "p" }: Props = $props();
</script>

<svelte:element this={as} class="{className} {type} {styles[type]}">
  {#if children}
    {@render children()}
  {/if}
  
</svelte:element>