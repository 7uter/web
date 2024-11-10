<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Game Download Website</title>
    <link rel="stylesheet" href="/css/style.css">
</head>
<body>
    <header>
        <h1>Welcome to Game Download Website</h1>
        <form action="/search" method="GET">
            <input type="text" name="query" placeholder="Search games...">
            <button type="submit">Search</button>
        </form>
    </header>
    <section id="games">
        <% games.forEach(game => { %>
            <div class="game">
                <img src="<%= game.image %>" alt="<%= game.title %>">
                <h2><%= game.title %></h2>
                <p><%= game.description %></p>
                <a href="/games/<%= game._id %>">Download</a>
            </div>
        <% }) %>
    </section>
</body>
</html>
