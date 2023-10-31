<!-- FILEPATH: /c:/Users/timon/OneDrive/Documents/Svelte/watchlist/src/routes/aboutMe.svelte -->

<script>
    let tableData = [
        { name: 'John', age: 25, city: 'New York' },
        { name: 'Jane', age: 30, city: 'Los Angeles' },
        { name: 'Bob', age: 40, city: 'Chicago' },
        { name: 'Alice', age: 35, city: 'Houston' },
    ];
</script>

<nav>
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>

<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Age</th>
            <th>City</th>
        </tr>
    </thead>
    <tbody>
        {#each tableData as item}
            <tr>
                <td>{item.name}</td>
                <td>{item.age}</td>
                <td>{item.city}</td>
            </tr>
        {/each}
    </tbody>
</table>

<style>
    nav {
        background-color: #333;
        color: white;
        padding: 10px;
    }
    
    nav ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;
    }
    
    nav li {
        float: left;
    }
    
    nav li a {
        display: block;
        color: white;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
    }
    
    table {
        border-collapse: collapse;
        width: 100%;
    }
    
    th, td {
        text-align: left;
        padding: 8px;
    }
    
    th {
        background-color: #333;
        color: white;
    }
    
    tr:nth-child(even) {
        background-color: #f2f2f2;
    }
</style>
