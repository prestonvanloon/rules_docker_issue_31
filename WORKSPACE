git_repository(
    name = "io_bazel_rules_docker",
    remote = "https://github.com/bazelbuild/rules_docker.git",
    commit = "6064bb5f84553d56222e66f154a5f8a434f220ab",
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
