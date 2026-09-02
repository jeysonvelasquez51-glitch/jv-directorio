# jv-directorio

Directorio de despachos judiciales de la suite **Justicia Virtual · LegalTools**,
publicado para que las herramientas se actualicen solas.

## Qué hay aquí

| Archivo | Qué es |
|---|---|
| `directorio.jvd` | El directorio, **cifrado**. ~2,1 MB |
| `version.json` | Fecha de generación y número de despachos |

Las apps consultan `version.json` una vez al día y descargan `directorio.jvd` cuando la
fecha de generación avanza.

## Sobre el cifrado

`directorio.jvd` **no es legible sin una licencia de Justicia Virtual**. Va cifrado con una
clave que solo transportan las licencias emitidas, así que descargarlo sin ella no aporta
nada: son unos megas de ruido.

El archivo además está **autenticado** (HMAC): cualquier modificación lo invalida y las
apps lo rechazan sin llegar a instalarlo.

## Actualizar (solo el autor)

1. Correr la tarea mensual que regenera el directorio.
2. Pulsar **«Cifrar directorio»** en la herramienta de licencias — genera los dos archivos.
3. Reemplazarlos aquí y hacer commit.

Los usuarios no tienen que hacer nada.

---

Repositorio de datos: no contiene código. El código de la suite es privado.
