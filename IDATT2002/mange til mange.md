>[!eksempel]
>create table game_user(
>username VARCHAR(100),
>game_id int,
>primary key(username, game_id),
>foreign key(username) references users(username) on delete cascade,
>foreign key(game_id) references games(game_id) on delete cascade);

Hvis du ønsker en mange til mang relasjon må du lage en spesiel koblingstabell som knytter de to tabellene