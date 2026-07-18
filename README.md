# walle

> Skill para Claude Code que **piensa contigo** en vez de construir por ti. Cuando ya decidiste qué vas a hacer y necesitas ideas, walle abre el abanico, las tensiona y te deja con la mejor — no con la primera.

## El problema

Sueltas una idea sobre algo que ya decidiste hacer, y Claude arranca a ejecutar: te propone una solución y escribe el código. Se siente productivo. Y mata la parte más valiosa —abrir el abanico— antes de que empiece. Te quedas con la primera idea razonable en vez de la mejor.

El otro extremo es igual de malo: una lluvia de ideas sin cerca ni final es dispersión con buen formato. Quince opciones bonitas que no vas a construir.

walle vive en el medio.

## Qué hace esta skill

walle es el paso que **diverge**, el que casi nunca tiene casa:

**divergir (walle) → juzgar (validador) → planificar → construir**

Cuando dices `/walle` (o "es una lluvia de ideas", "dame opciones para…"), Claude deja de ejecutar y se pone a pensar contigo:

1. **Planta la cerca** — antes de tirar una sola idea, exige la frase que enmarca todo: *qué trabajo ya decidido, para qué, y qué no se puede tocar*. Sin cerca, no hay lluvia.
2. **Diverge** — rebota tu idea, tira caminos que se contradicen, deja volar hasta lo absurdo. Sigue abierto mientras aparezcan **direcciones nuevas**, no variaciones de lo mismo.
3. **Cierra con criterio** — la lluvia termina cuando hay un candidato que te prende **y** que cubre el "para qué". Ni antes (enamorarte de la primera) ni nunca (dar vueltas para no arrancar).
4. **Reparte por tres puertas** — el ganador va al validador; el resto se borra, o se guarda solo si tiene una condición concreta para resucitar.

No se dispara sola en cada respuesta. Solo cuando la invocas o pides ideas dentro de un trabajo decidido.

## El diferencial: la cerca y el portón duro

Lo que separa a walle de "Claude conversando" es que **no te deja saltarte la cerca**.

Una lluvia de ideas sin marco es la máquina de dispersión perfecta. walle lo impide con una regla dura: **no vuela ninguna idea hasta que exista el trabajo decidido + el para qué + lo que no se mueve**. Puedes armar esa cerca en la mesa, ahí mismo, pero tiene que estar antes de la primera idea.

Eso convierte la lluvia en algo que produce, en vez de algo que te entretiene. Y como descartar es el default —guardar una idea cuesta nombrar su condición de resucitar—, el cuaderno no se te llena de un cementerio de "ideas futuras" que nadie relee.

## Instalación

### Opción A — Skill global (recomendada)

```bash
git clone https://github.com/hildemarosolis/walle.git ~/.claude/skills/walle
```

Reinicia Claude Code. Disponible en todas tus sesiones.

### Opción B — Symlink desde repo local

```bash
git clone https://github.com/hildemarosolis/walle.git ~/REPOS/walle
ln -s ~/REPOS/walle ~/.claude/skills/walle
```

Ventaja: editas el `SKILL.md` en el repo y los cambios se reflejan al instante.

## Uso

```
/walle
```

Sobre algo que ya decidiste hacer. O directo:

```
Voy a cambiar cómo funcionan las tareas en mi sistema. /walle
```

walle te pedirá la cerca antes de tirar la primera idea. Es a propósito.

## Qué NO hace

- **No es el validador.** walle abre opciones; el validador juzga una y da GO/NO-GO. walle le entrega el ganador.
- **No decide si hacer algo.** Eso es go/no-go = validador. walle entra cuando el trabajo YA está decidido.
- **No planifica ni escribe código.** Para el plan, `agent-skills:plan`. Para construir, el flujo normal.
- **No te sirve un menú.** Piensa contigo y te saca tus propias ideas; no lista opciones para que escojas.

## Licencia

MIT. Ver [LICENSE](LICENSE).
