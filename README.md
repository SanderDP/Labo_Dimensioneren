# Labo Dimensioneren

Gedeelde repository voor het labo Dimensioneren van Machines.
De bibliotheek `rm_python_lib` (KU Leuven GitLab) zit erin als **git submodule**.

## Eerste keer clonen

```bash
git clone --recurse-submodules https://github.com/SanderDP/Labo_Dimensioneren.git
```

Al gecloned zonder submodule (map `rm_python_lib` is leeg)?

```bash
git submodule init
git submodule update
```

## Library gebruiken

Maak je eigen bestanden/mappen in de root van deze repo en importeer via `rm_python_lib.`, bv.:

```python
from rm_python_lib.MechDesign.Units.Units import m_, mm_, kg_, s_, N_, rpm_, W_, deg_
```

## Regels

- Wijzig **niets** in de map `rm_python_lib/` — je kan daar niet naar pushen.
- Library updaten naar de nieuwste versie:

  ```bash
  git submodule update --remote
  git commit -am "update rm_python_lib"
  git push
  ```
