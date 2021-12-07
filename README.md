### Conceptos de Git Ramas:

El siguiente comando nos ayuda a crear una rama en nuestro repositorio git el nombre de la
rama no debe contener caracteres extraños ni espacios en blanco.

git branch nombre_rama

### El puntero HEAD:

El puntero HEAD es quien le dice a git en que rama te encuentras en cada momento.

Imagina que tienes dos ramas master y testing , las ramas siempre deben apuntar a un
commit .

### Ubicando nuestro HEAD

3. Si en algún momento no sabes donde se encuentra tu HEAD puedes usar el comando:

git log

4. Si realizo otro cambio en mi proyecto (en mi README.md ) y creo un nuevo commit . Podemos
visualizar como nuestro HEAD continua avanzando con main
5. Si cambio de rama usando el comando git checkout testing y realizo un git log puedo
notar como el HEAD cambia de posición.

6. Git tiene una forma de visualizar tus ramas por terminal, resulta muy útil cuando quieres ver
un panorama general de tu proyecto.

git log --oneline --decorate --graph --all

7. Unir ramas, cuando deseas combinar el trabajo realizado en dos ramas distintas debes
hacer lo siguiente:
Debes moverte a la rama destino, en nuestro caso la rama main , usando el comando git
checkout main .
Luego debes usar el comando git merge testing para unir la rama testing con la main
Si has estado modificando el archivo README.md cada vez que haces un commit en las
distintas ramas es muy probable que tengas un conflicto al unir las ramas. Este tipo de
conflicto se presenta de la siguiente manera.