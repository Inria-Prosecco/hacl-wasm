# hacl-wasm

## How to extract HACL* to wasm

1. Clone the [F*](https://github.com/FStarLang/FStar) repo, switch to branch `master`.

  * In the repo directory, enter:
  ```
  cd src/ocaml-output && make
  cd ../../ulib/ml && make
  ```
  * Set the `FSTAR_HOME` environment variable to the location of F* repo.

2. Clone the [KreMLin](https://github.com/FStarLang/kremlin) repo, switch to branch `fstar-master`. In the repo, build with `make` and set the `KREMLIN_HOME` environment variable to the location of the Kremlin repo.

3. Clone the [HACL*](https://github.com/mitls/hacl-star) repo, switch to the  `fstar-master` branch. In the repo, build with `make build` and set the `HACL_HOME` environment variable to the location of the HACL* repo.

4. Go to the KreMLin repo and its `test` directory. Test the wasm extraction  with `make wasm`. You can then extract individual files with :

  ```
  make $HACL_HOME/code/curve25519/Hacl.Test.X25519.wasm
  ```
