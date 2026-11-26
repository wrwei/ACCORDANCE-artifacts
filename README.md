# ACCORDANCE paper artifacts

Reproducibility files for *Machine-checked consistency of fault signatures for
model-based safety analysis and diagnosis*.

## Release files

Download the three archives and `SHA256SUMS` from the same version in
[GitHub Releases](https://github.com/wrwei/ACCORDANCE-artifacts/releases).

| Archive | Contents and starting point |
| --- | --- |
| `reviewer-bundle.tar.gz` | System models, analysis code, Isabelle sessions and build logs, and the mutation and independent checks. Start with `reviewer-bundle/REVIEWERS.md`. |
| `dxc10-grouped-evaluation.zip` | ADAPT-Lite detection and diagnosis replays, the five-detector comparison, and per-run results. Follow the archive's `README.md` with the reviewer bundle extracted alongside it. |
| `darmstadt-hardware-evaluation.zip` | Hydraulic rig evaluator, recording manifest, and per-run results. Follow the archive's `README.md`. |

## Verify and extract

Run these commands in the directory containing the release downloads.

```sh
shasum -a 256 -c SHA256SUMS
tar -xzf reviewer-bundle.tar.gz
unzip dxc10-grouped-evaluation.zip -d dxc10-grouped-evaluation
unzip darmstadt-hardware-evaluation.zip -d darmstadt-hardware-evaluation
```

Each hardware guide gives the source and integrity checks for its raw
recordings. The [corrected NASA DXC'10 archive](https://c3.ndc.nasa.gov/dashlink/static/media/dataset/DXC10_DP1Comp20110818.zip)
supplies the ADAPT-Lite runs. The [TU Darmstadt data repository](https://tudatalib.ulb.tu-darmstadt.de/handle/tudatalib/5478)
supplies the hydraulic rig runs.
