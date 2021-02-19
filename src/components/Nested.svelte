<script>
    let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<p>
    This is my first nested svelte component., comps are capitalized so can be
    diferentiated from html tags
</p>
<p>
render an input of string into stylized HTML (using a tag):
    {@html string}
</p>