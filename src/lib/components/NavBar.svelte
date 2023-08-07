<script>
	export let name = 'Home';
	export let link = '/';
</script>

<a
	class="  hover:bg-gray-200 py-2 px-4 rounded-md transition-all duration-300 group flex items-center gap-1"
	href={link}
>
	<span class=" font-medium">{name}</span>
</a>
