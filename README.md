<!-- GENERATED from polynomial_evaluation/bn254@1.0.0. Do not edit — `--update` rewrites it. -->
# A polynomial at a point, over BN254 scalar field elements

An answer to `polynomial_evaluation/bn254@1.0.0`, in rust.

## What you write

`src/solve.rs`, and nothing else.

```
init(Point)         -> state     setup. Not measured.
run(state, Inputs)  -> Outputs   the task. Measured, and only this.
free(state)                      optional.
```

`init` never sees the data, so there is nothing for it to compute ahead of
time. Reading the case and writing the answer happen outside the measured
call, in generated code — which is why seeing the inputs early is not a way
to answer early.

## The shapes

- `coeffs` — tensor<N x L x u64>
- `x` — tensor<L x u64>
- `q` — tensor<L x u64>
- returns `y` — tensor<L x u64>

## Generated, and not yours

Every file but the one above carries a header saying so. They are rewritten
by `fherma implementation init --update`, which never touches yours.
