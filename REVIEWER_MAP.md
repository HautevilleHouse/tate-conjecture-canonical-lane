# Reviewer Map

## Claim Scope

- Canonical-lane claim: inside the `manifold_constrained` lane, if the theorem chain in this repository holds and the guard certificate passes, the repository-level closure claim is satisfied.
- Standard target claim: carried by the in-repo bridge theorems tying the lane to the target statement.
- External-strengthening rule: any statement beyond the admissible class must retain the explicit remainder carried by the defect/coherence ledgers; see `notes/GEOMETRIC_GALOIS_BRIDGE.md`.

## Theorem Dependency Chain

1. `EG1`: coercive response and active control floor.
2. `EG2`: capture and admissible continuation.
3. `EG3`: compactness and no-collapse spacing.
4. `EG4`: rigidity and transfer.
5. Identification bridge: strict coherence on the determining class.
6. Scalar closure: `TATE_G1, TATE_G2, TATE_G3, TATE_G4, TATE_G5, TATE_G6, TATE_GM` all `PASS`.

Primary files:

- `paper/TATE_CONJECTURE_PREPRINT.md`
- `notes/EG1_public.md`
- `notes/EG2_public.md`
- `notes/EG3_public.md`
- `notes/EG4_public.md`
- `notes/IDENTIFICATION_BRIDGE.md`
- `notes/GEOMETRIC_GALOIS_BRIDGE.md`

## Closure Gates

| Gate | Constant | Description |
|------|----------|-------------|
| `TATE_G1` | `kappa_cycle` | projected cycle-class response has a strict positive floor |
| `TATE_G2` | `sigma_frobenius` | Frobenius defect stays above capture floor across admissible correspondence losses |
| `TATE_G3` | `kappa_compact` | normalized near-failure families are precompact and cycle windows do not collapse |
| `TATE_G4` | `rho_rigidity` | bad nonalgebraic countermodels are excluded |
| `TATE_G5` | `class_transfer` | rigid limit transfers to the algebraic-cycle endpoint class |
| `TATE_G6` | `eps_coh` | strict coherence / identification closure |
| `TATE_GM` | derived | final strict margin |

## Falsification Conditions

- `repro/certificate_runtime.json` has any non-`PASS` gate.
- `lane.active_lane != "manifold_constrained"`.
- `all_pass != true`.
- Any manifest hash mismatch under `repro/repro_manifest.json`.
- A verified counterexample to any EG theorem statement used in the paper.
