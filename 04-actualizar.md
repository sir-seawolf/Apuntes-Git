# Actualizar 

## Uso de merge/pull, como mantener actualizados mis cambios

Cuando trabajamos en equipo, necesitamos tener actualizados nuestro repositorio en la rama en la que estemos trabajando para evitar tener muchos conflictos al final de nuestro desarrollo, es mucho más sencillo actualizar poco a poco los cambios que los demás desarrolladores están mergeando en la rama **dev** para así poder resolver los conflictos (si los tuviésemos) de una manera mucho más trivial: divide y vencerás.



### merge

Podemos usar el comando **merge**. Con este comando podremos mezclar los cambios de otros desarrolladores con los nuestros, por ejemplo:

```
$ git checkout ramaA
$ proyecto - ramaA > git merge ramaB

```

En este ejemplo estamos cambiandonos de rama, a la rama `ramaA` y estamos mezclando la rama `ramaB` en ella.

### pull

Podemos usar el comando **pull**. Con este comando podremos traermos los cambios de otros desarrolladores de cualquier repositorio enlazado a nuestro repositorio local en la rama que necesitemos y mezclarlos con nuestros cambios, por ejemplo:

```
$ git pull zero dev

```
Notemos entonces que el **pull es un fetch más un merge** en la misma operación.

Es posible que al traernos estos cambios podamos tener conflictos en nuestros cambios y los de otros desarrolladores. Esto se debe a que ambos abrimos rama en el mismo punto en la rama dev, con lo cual, el merge automático no sabe exactamente con qué cambio de cuál commit quedarse, ya que ninguno en principio estaría por encima del otro.

Cuando tenemos esta situación tendremos que hacer un merge manual, normalmente con una herramienta configurada para ello.
