# ZG ZoneGods 2.1.5 — configuration / configuración

The protected 2.1.5 JAR generated these exact files on isolated Forge 47.4.10. / El JAR protegido 2.1.5 generó estos archivos en Forge aislado.

| File / Archivo | Active values / Valores activos | Reload / Recarga |
|---|---|---|
| `config/zonegods-common.toml` | `[staff] damage` (1–100, default 25), `attackSpeed` (0.1–10, default 1.6), `lightningCooldownTicks` (0–12000, default 40). | `/zonegods reload` reads this Forge config and writes the values to world saved data and the ZONEMODS mirror. / Lee esta configuración y actualiza los datos del mundo y el espejo. |
| `config/ZONEMODS/zonegods/baculo/ajustes.toml` | `[baculo] dano`, `velocidad_ataque`, `recarga_ticks`; `permiso_uso` and `permiso_admin` are informational strings, not editable permission rules. | `/zonecore reload` reads the three numeric values, saves them in world data, then regenerates this file. / Lee tres valores numéricos, los guarda en el mundo y regenera el archivo. |

`/zonegods config info` reports current world-saved values. `/zonegods config staff_damage <1–100>`, `staff_speed <0.1–10>` and `staff_recarga <0–12000>` change world-saved values and regenerate `ajustes.toml`. A later `/zonegods reload` will override them from `zonegods-common.toml`; a later `/zonecore reload` will override them from `ajustes.toml`. Keep both files aligned if you use both reload commands. / Mantén los dos archivos sincronizados si usas ambos comandos de recarga.

There are no recipes in this version. / No hay recetas en esta versión. Back up the world before changing persistent staff settings. / Respalda el mundo antes de cambiar valores persistentes del báculo.

