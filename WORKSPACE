git_repository(
    name = "io_bazel_rules_docker",
    remote = "https://github.com/bazelbuild/rules_docker.git",
    commit = "df9d21334be0d45b6995f5f46024a3d2ea22eca9", 6/15/17
)

load(
  "@io_bazel_rules_docker//docker:docker.bzl",
  "docker_repositories", "docker_pull"
)
docker_repositories()

docker_pull(
  name = "java_base",
  registry = "index.docker.io",
  repository = "openjdk",
  tag = "8"
)
