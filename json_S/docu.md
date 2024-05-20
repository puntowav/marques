# Documentació de l'API del Escape Room del Picapollo

## Descripció General

L'API del Escape Room del Picapollo està dissenyada per proporcionar una experiència interactiva en la qual els usuaris poden navegar a través de diferents ubicacions i realitzar diverses accions per progressar en el joc. A continuació, es presenten els aspectes generals sobre com utilitzar aquesta API.

## Endpoints Principals

### 1. `/start`
- **Descripció**: Introducció al joc.
- **Contingut**:
  - Missatge de benvinguda.
  - Regles bàsiques del joc.
  - Instruccions generals sobre l'ús de l'API.
  - Mapa de la casa.

### 2. `/salon`
- **Descripció**: Punt de partida dins de la casa.
- **Contingut**:
  - Mapa del saló.
  - Descripció del saló.
  - Opcions de navegació (garatge, escales, armaris).

### 3. `/garaje` i `/garaje_8`
- **Descripció**: Accés al garatge i el seu contingut.
- **Contingut**:
  - Missatge indicant la necessitat d'una clau per obrir el garatge.
  - Descripció del garatge i objectes interactius (maleter, porta del darrere, prestatge, etc.).

### 4. `/armario_rojo` i `/armario_azul`
- **Descripció**: Contingut dels armaris al saló.
- **Contingut**:
  - Objectes trobats dins dels armaris.
  - Accions possibles amb els objectes (per exemple, utilitzar una clau per obrir el garatge).

### 5. `/escalera` i `/escalera_7`
- **Descripció**: Accés als diferents pisos de la casa.
- **Contingut**:
  - Descripcions dels pisos i opcions per navegar a diferents habitacions.

### 6. `/primer_piso` i `/segundo_piso`
- **Descripció**: Navegació pels pisos superiors.
- **Contingut**:
  - Mapes dels pisos.
  - Descripcions de les habitacions i objectes dins d'elles.

### 7. `/habitacion_padre` i `/habitacion`
- **Descripció**: Accés a les habitacions individuals.
- **Contingut**:
  - Objectes i accions dins de les habitacions.
  - Opcions per tornar a altres punts de la casa.

## Accions i Mètodes

### Mètodes GET
- Utilitzats per obtenir informació sobre les diferents ubicacions i objectes.
- Exemple: `GET /salon`, `GET /armario_azul`.

### Mètodes POST, PUT, PATCH, DELETE
- **POST**: Afegir nous elements.
  - Exemple: `POST /cazuela` amb un nou ingredient.
- **PUT**: Actualitzar informació existent.
  - Exemple: `PUT /cazuela` per canviar un ingredient.
- **PATCH**: Modificar parcialment un objecte.
  - Exemple: `PATCH /cazuela` per afegir un nou ingredient.
- **DELETE**: Eliminar objectes específics.
  - Exemple: `DELETE /caca` per tirar de la cisterna.

## Solucions i Progressió

### Ruta a Seguir per Acabar el Joc
1. **Saló**: Comença al saló (`/salon`).
2. **Armari Blau**: Ves a l'armari blau i fes un `DELETE` de la id: "llave" (`/armario_azul`).
3. **Garatge**: Entra al garatge (`/garaje_8`).
4. **Porta del Darrere**: Ves a la porta del darrere (`/puerta_trasera`).
5. **Bossa Esportiva**: Ves a la bossa esportiva (`/bolsa_deportiva`).
6. **Cazuela**: Fes un `POST` del pollastre en la cazuela (`/cazuela`).
7. **Escales**: Torna al saló i puja les escales (`/escalera_7`).
8. **Primer Pis**: Ves al primer pis (`/primer_piso`).
9. **Segon Pis**: Ves al segon pis (`/segundo_piso`).
10. **Habitació**: Entra a l'habitació (`/habitacion`).
11. **Mesita de Noche**: Ves a la mesita de noche i fes un `POST` del llimó (`/mesita_de_noche`).
12. **Bany**: Entra al bany (`/baño_9`).
13. **Maquina de Raigs X**: Ves a la màquina de raigs X i fes un `POST` del "tostón" (`/maquina_de_rayos_X`).
14. **Cazuela**: Finalment, ves a la cazuela (`/cazuela_173`) i després menja (`/comer_999`) per guanyar el joc.

Aquesta documentació proporciona una visió general de com utilitzar l'API del Escape Room del Picapollo. Per a detalls específics sobre cada endpoint i les dades exactes, es recomana explorar els JSON associats a cada secció.
