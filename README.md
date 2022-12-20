# solver-playground

Troubleshooting how/why `micromamba` solves so much faster than `mamba` on my computer.

For me...

`Dockerfile.micromamba` - **~2.5 minutes**

```shell
docker build -t solve-with-micro -f Dockerfile.micromamba .
```

`Dockerfile.mamba` - **~12 minutes**

Using an installed `mamba` as the solver takes... awhile.

```shell
docker build -t solve-with-mamba -f Dockerfile.mamba .
```

`Dockerfile.micro_and_mamba` - **fails to solve**

Uses `micromamba`, installs `mamba`, and passes the path to `conda-lock` as the solver.

```shell
docker build -t solve-with-micro-and-mamba -f Dockerfile.micro_and_mamba .
```
