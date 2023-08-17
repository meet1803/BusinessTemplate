<script>
	export let name = '';
	export let link = '';
</script>

<a
	class="py-2 px-4 rounded-md group lg:flex hidden items-center "
	href={link}
>
	<span class=" font-normal text-left">{name}</span>
</a>
