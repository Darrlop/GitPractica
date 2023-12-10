#################################
    CUESTIONARIO PRÁCTICA GIT
      --Editado con VIM--
#################################

NOTA: Alberto, al usar git log --graph  he añadido la opción --all porque en windows tenía alguna pega
para que me saliera el gráfico y si le añadía --all iba bien
 


- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

git reset --hard HEAD~1
Mueve la rama actual y el puntero HEAD al commit padre, y además restablecemos el área de trabajo
también al del commit padre


- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

Busco el id del commit con git reflog

git reset --hard 6bf767c
		 (id commit)


- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No. Al realizar este merge lo que hacemos es dar a la rama styled (que está siendo apuntada
por HEAD), acceso a los commits de la rama main. Al ser styled hija de main, no produce
ningún conflicto 


- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

En este caso sí: el merge se hace entre 2 ramas, cada una de las cuales contiene commits que reflejan cambios
en las mismas líneas del fichero git-nuestro.md; de ahí el conflicto


- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No. Al poder hacerse un merge fast-forward, lo que se hace es mover la rama main y el puntero HEAD a la rama styled.
Se tiene acceso a los comits sin producirse ninguna confusión entre las versiones del documento.


- ¿Qué comando o comandos utilizaste en el paso 25?

git log --graph --all


- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Inicialmente, según entiendo la pregunta,No. Si queremos que sea main quien absorva a title, perderíamos su commit. 
Como un fast forward mueve la rama en la que está el HEAD hasta el commit de la rama que le indiquemos, para poder 
hacer un fast foward deberíamos pasar main y head al commit al que apunta title (se adjunta diagrama paso25 para 
ver la situación antes del merge).
 
 
- ¿Qué comando o comandos utilizaste en el paso 27?

git reset HEAD~1


- ¿Qué comando o comandos utilizaste en el paso 28?

git restore git-nuestro.md


- ¿Qué comando o comandos utilizaste en el paso 29?

git branch -D title


- ¿Qué comando o comandos utilizaste en el paso 30?

git reflog: para tener el log completo de cambios y recorridos del puntero HEAD

git reset --hard 9632b8e : para hacer un reset completo al commit obtenido del estudio de reflog


- ¿Qué comando o comandos usaste en el paso 32?

git log --graph --all

git reset --hard 9549589
		 (id del commit)


- ¿Qué comando o comandos usaste en el punto 33

git reflog

git reset --hard 2d406dc
		  (id del commit)

