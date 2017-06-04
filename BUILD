load("@io_bazel_rules_docker//docker:docker.bzl", "docker_build")

java_binary(
    name = "my-runner",
    srcs = glob(["src/main/java/com/example/*.java"]),
    main_class = "com.example.ProjectRunner",
)

docker_build(
	name = "docker",
	# ERROR: /tmp/test/BUILD:9:1: //:docker: expected value of type 'string' for attribute 'base' in 'docker_build_' rule, but got ["@java_base//image:image.tar"] (list).
	# base = ["@java_base//image:image.tar"],
	base = "@java_base//image:image.tar",
	cmd = "java -jar my-runner_deploy.jar",
	files = [
		":my-runner_deploy.jar",
	],
)
