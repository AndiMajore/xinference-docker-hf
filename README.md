# xinference-docker-hf

This project allows easy deployment of any huggingface LLM using [xinference](https://github.com/xorbitsai/inference) and docker.

## Get started

1. Install docker and docker-compose (now also 'docker compose') on your machine.
2. Install nvidia-docker libraries (find details about the Nvidia-Container Toolkit [here](https://hub.docker.com/r/nvidia/cuda))
3. Copy the [env.example](https://github.com/AndiMajore/xinference-docker-hf/blob/master/llama2_7b_chat_hf.env.example) file to e.g. llama2_7b_chat_hf.env and set the 'HF_TOKEN_READ' environment variable to your [huggingface access token](https://huggingface.co/settings/tokens).
4. Run `docker-compose build && docker-compose up -d`. This should build and start a container in the background that downloads and runs the llama2_7b model (if you have access)
5. Optional: Depending on what you want to run from huggingface you need to adjust the (xinference) config file, the env file or even the download_register_and_launch.sh file.
