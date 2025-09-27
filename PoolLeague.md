#### Welland Pool League Tracker

This is a site I created to track the Welland Pool League standings, player statistics, schedules, and match results. As the league administrator has not yet adopted this site, I have been using it to track my teams statistics.

We are going to try and push for this to be used for the 2025/2026 season. This will allow all players to view their statistics, standings, schedules and match results instead of waiting for the league administrator to post updates in the facebook group twice per season.

This was created in Blazor, using C# and the MudBlazor Compontent Library. I also use a Microsoft SQL Server database to store the data. I was using an API to serve the data but opted to use DataFactories instead to simplify the architecture and the performance is much better. I am using Auth0 for authentication and authorization. This allows me to easily manage users and roles. There is an administration area where I can manage teams, players, schedules, and statistics. The Team Standings show the three Divisions the league has and the teams will show in the appropriate division based on number of weeks/games won.

Click the image below to visit the site.

[![Welland Pool League Preview](Images/WPLPreview.png)](https://wpl.codersden.com)
