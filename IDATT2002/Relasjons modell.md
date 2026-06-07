En relasjonsmodell er bare en måte og skrive opp tabllene dine:
>[!eksempel]
>bok(__bokid__, text, utgivelses år, forfatterid*)
>forfatter(__forfatterid__, navn)

Over er et eksempel på en mange til en relasjon(1:n) flere bøker kan ha fremmed nøkkelen som peker til samme forfatter id. Altså en forfatter har flere bøker

Vi kan også ha en mange til mange relasjon
>[!eksempel]
>artist(__artistnavn__,fødselsår)
>sang(__sangid__, tekst)
>artist_sang(artistnavn*,sangid*)