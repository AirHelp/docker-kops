# docker-kops

Kops Docker Images based on Alpine Linux.

# What is kops?

Kops is a tool to lets you deploy production-grade, highly available, Kubernetes clusters from the command line.

  * [Kops on GitHub](https://github.com/kubernetes/kops)

# Usage

```
docker run --rm -it \
  -e AWS_REGION \
  -e AWS_PROFILE \
  -e KOPS_STATE_STORE \
  -v "$HOME"/.ssh:/root/.ssh:ro \
  -v "$HOME"/.aws:/root/.aws:ro \
  -v "$HOME"/.kube:/root/.kube:rw \
  -v "$(pwd)":/workdir \
  -w /workdir \
  airhelp/kops "$@"
```
