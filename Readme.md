## Postgres Exercici 4

1 - Seguiu l'exemple explicat: creant la taula Cities i Capitals. Proveu de fer insercions en ambdues taules i veure els resultats.

<ul>
  <li>Creem les taules,cities i capitals amb herencia<br><img src="https://github.com/Xavi678/Postgres4/blob/master/imatges/Selecci%C3%B3n_002.png"/><br></li><li>Inserim dades<br><img src="https://github.com/Xavi678/Postgres4/blob/master/imatges/Selecci%C3%B3n_003.png"/><br>
  <img src="https://github.com/Xavi678/Postgres4/blob/master/imatges/Selecci%C3%B3n_004.png"/><br>
  <img src="https://github.com/Xavi678/Postgres4/blob/master/imatges/Selecci%C3%B3n_005.png"/></li>
  <li>Podem veure que quan inserim informació en la taula capitals, podem inserir camps de les cities degut a l'herencia, i que quan inserim informació a la classe capitals, aquesta també s'inserta a la classe cities</li>
 
</ul>

2 - Per què creieu que s'utilitza el tableoid ? i el pg_class ?
- S'utilitzen per obtenir informació sobre les taules, podem obtenir l'Id de la taula, una taula amb herencia tindrà el mateix id que el seu pare, i per tant podrem veure l'herència

3 - Al llegir la documentació. Penseu que es pot utilitzar l'herència múltiple en Postgres ? Fiqueu algun exemple
- <img src="https://github.com/Xavi678/Postgres4/blob/master/imatges/Selecci%C3%B3n_006.png"/> Si, com podem veure en aquest exemple una taula pot heredar d'una o més taules

4 - Identifiqueu algunes limitacions de l'herència en Postgres. 
Estudieu com es propaguen les foreign keys o els canvis de taules etc.. d'una classe "pare" o superclasse a les seves classes "filles". 
Podeu consultar per les instruccions:SELECT, UPDATE, DELETE, ALTER TABLE,  ALTER TABLE ... RENAME, vauum, reindex).
- A l'hora de fer un delete si es borra del fill també ho fa del pare, quan executes un insert a la taula fill també s'inserta a la taula pare, i lo mateix quan es fa algun update ja que les taules tenen el mateix id.
