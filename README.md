# RheMAP-Surf resources

Macaque template surfaces, cortical maps, and spherical registrations for surface
resampling and neuromaps-prime integration.

## Contents

| Location | Contents |
| --- | --- |
| `surfaces/<space>/` | 50 template surface files and 48 curvature/thickness/sulc/cortexmask maps |
| `alignments/` | 60 registration spheres: 30 directed routes among the six main templates, for both hemispheres |

There are 158 GIFTI files in total.

| Template | Mesh density |
| --- | --- |
| CIVETNMT | 41k |
| D99 | 41k |
| MEBRAINS | 101k |
| NMT2Sym | 41k |
| NMT2Asym | 41k |
| Yerkes19 | 32k |
| F99 | 74k |

CIVETNMT has no supplied pial surface. F99 includes only sphere and midthickness
surfaces. Cortex masks use `1=cortex` and `0=medial wall`. The `sulc` maps contain
DPF-derived fields (brain-slam 0.1.2; alpha=0.03). Thickness maps use FreeSurfer
with neighborhood size 20; CIVETNMT uses twice the white-to-midthickness distance.

## Registration and resampling

Registration spheres are named
`src-<source>_to-<target>_den-<source-density>_hemi-<L|R>_sphere.surf.gii`.

Each retains the source mesh and represents its correspondence in the target
spherical parameterization. For source-to-target resampling, use the registration
sphere as the current sphere and the supplied target sphere as the new sphere.
Use the source and target midthickness surfaces for area-corrected metric
resampling.

## F99–Yerkes19 legacy registration

The F99 74k spheres retain F99 vertex indexing and encode the published
F99-to-Yerkes19 registration from
[BALSA](https://balsa.wustl.edu/reference/show/976nz).

For F99-to-Yerkes19 resampling, use the F99 sphere as the current sphere and the
supplied Yerkes19 32k sphere as the new sphere. Exchange these roles for the reverse
direction. Both directions reuse these existing sphere files. See
[surfaces/F99/README.md](surfaces/F99/README.md) for provenance and references.

## Sources

[RheMAP-Surf](https://github.com/HumanBrainED/RheMAP-Surf) ·
[RheMAP-Surf dataset](https://doi.org/10.5281/zenodo.15642802) ·
[BALSA F99–Yerkes19 resources](https://balsa.wustl.edu/reference/show/976nz)
