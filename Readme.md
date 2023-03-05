# evcxr-jupyter-container

A containerized version of the [Evcxr](https://github.com/evcxr/evcxr), an evaluation context/REPL for Rust as a Jupyter kernel.

## Usage

1. Build it yourself by cloning this repo:
    ```sh
    git clone  https://github.com/cheperuiz/docker-evcxr
    cd docker-evcxr
    podman build -t evcrx_jupyter
    podman run -w /scripts -v ./notebooks:/notebooks -p 8888:8888 -u 1000:1000 localhost/evcrx_jupyter
    ```
2. Go to `http://localhost:8888`
3. Check blocks in `evcrx-test.ipynb` to ensure kernel is running correctly.

Edited files are mapped from `/notebooks`
