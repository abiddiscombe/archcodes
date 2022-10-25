<!-- src/lib/Header.svelte -->

<script>

</script>

<div>

    <header>
        <a id="logo" href="https://arch.codes">
            arch.codes
        </a>
        <nav>
            <ul>
                <li>
                    <a href="https://github.com/abiddiscombe">
                        <i class="bi bi-github" />
                    </a>
                </li>
                <li>
                    <a href="https://linkedin.com/in/archiebiddiscombe">
                        <i class="bi bi-linkedin" />
                    </a>
                </li>
            </ul>
        </nav>
    </header>

</div>

<style>

    div {
        margin: 0;
        padding: 0;
    }
    
    header {

        margin: 0;
        padding: 1em;

        display: flex;
        flex-wrap: wrap;
        align-items: center;
        flex-direction: row;
        justify-content: space-between;

    }

    header > a {

        margin: 0;
        padding: 0;

        color: inherit;

        font-size: 1em;
        font-weight: 600;
        font-family: var(--font-family);

        text-decoration: none;

    }

    header > nav {

        margin: 0;
        padding: 0;

    }

    header > nav > ul {

        margin: 0;
        padding: 0;

        list-style-type: none;

        display: flex;
        flex-wrap: wrap;
        align-items: center;
        flex-direction: row;
        justify-content: start;

    }

    header > nav > ul > li {
        
        margin: 0;
        padding: 0;

    }

    header > nav > ul > li > a {

        margin: 0.4em 0em;
        padding: 0.6em;

        color: inherit;

        font-size: 1.2em;
        font-weight: 400;
        font-family: var(--font-family);

        text-decoration: none;

    }

    header > nav > ul > li > a:hover {

        transition-duration: 200ms;
        color: var(--accent);

    }


</style>