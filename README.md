# solver-playground

Troubleshooting how/why `micromamba` solves so much faster than `mamba` on my computer.

For me...

**~2.5 minutes**

```shell
docker build -t solve-with-micro -f Dockerfile.micromamba
```

**~12 minutes**

```shell
docker build -t solve-with-mamba -f Dockerfile.mamba
```
