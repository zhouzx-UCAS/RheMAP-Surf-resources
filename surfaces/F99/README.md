# F99 surface resources

Source: [BALSA — Macaque Cortical Parcellations and Yerkes19
MRI-based Atlas](https://balsa.wustl.edu/reference/show/976nz).
See the [F99 registration scene](https://balsa.wustl.edu/KlpmZ).

These four files are copied unchanged from
`RheMAP-Surf/templates/YRK/F99_74k_RegisteredToMY19/`
and renamed using this package's conventions. Original filenames:
`F99.[L/R].midthickness.native.surf.gii` and
`F99.[L/R].sphere.regMY19.native.surf.gii`.

Each hemisphere has 73,730 vertices. The midthickness surfaces retain
native F99 anatomical coordinates. The sphere files preserve F99
vertex indexing and are registered to the Yerkes19 v1.2 spheres.

Use these registered F99 spheres together with the corresponding
Yerkes19 spheres for F99-to-Yerkes19 resampling. Exchange the current
and new sphere roles for Yerkes19-to-F99 resampling.

References: Donahue et al. (2016), doi:10.1523/JNEUROSCI.0493-16.2016;
Donahue et al. (2018), doi:10.1073/pnas.1721653115.
