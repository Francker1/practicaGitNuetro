## Respuestas práctica Git

1. Usé **git reset --hard HEAD~1** para moverme al commit inmediatamente anterior y forzar con hard borrar también los cambios en tanto en el working copy como staging area.
2. Primero un **git reflog** para ver el SHA del commit donde apliqué los 'estilos' y seguidamente un **git reset --hard 'id_commit'** para traer los cambios al working copy también.
3. No, porque fue fast-forward y porque los commits están en una lista y no hay ramificaciones en el grafo.
4. Sí, hubo conflictos. Porque se tocaron mismas líneas en las mismas posiciones del archivo
5. No, porque previamente el conflicto fue resuelto, master absorve los cambios realizados en styled y e la rama master el archivo no habia sido previamente modificado.
6. **git log** para ver los commits realizados y el después lo volví a hacer con flag --graph para una renderización más "visual".
7. Sí, porque sólo se ha movido el puntero HEAD de master para que coincida con la de title. 
8. Primero un **git-log** para ver el commit anterior al merge y después un **git reset 'id_comit'**. Con esto, las ramas no están mergeadas pero no pierdo los cambios en el working copy.
9. **git-reset --hard HEAD~1** para descartar añadir el título al rezo, ahora el archivo está como cuando antes.
10. **git branch -D title** para borrar rama title.
11. Primero hice **git-reflog** para localizar el commit donde se mergea title en master y después **git checkout 'id_commit** para volver a ese commit, de esta forma cambia el punter HEAD a dicho commit. Seguidamente, un **git checkout -b title** para volver a crear la rama desde ese commit. Comprobé que, efectivamente, *master* NO tenía aún el título pero *title* sí. Finalmente me cambié a *master* e hice un merge con *title*. Ahora el rezo en *master* ya tiene el título que le puse.
12. Primero **git log** para ver los commits y seguidamente **git reset --hard 'id_commit'** para modificar lo que hay en el working copy y moverme haste ese commit.
13. **git reflog** para ver todos los commits y demás, seguidamente obtener el identificador simplificado (por ir probando) y hacer un **git reset --hard 'id_commit'** para mover HEAD hasta él. Ahora el archivo ya tiene el título y demás modificaciones.