load("@io_bazel_rules_go//go:def.bzl", "go_binary", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["manual-trigger.go"],
    importpath = "k8s.io/test-infra/experiment/manual-trigger",
    visibility = ["//visibility:private"],
    deps = [
        "//prow/github:go_default_library",
        "//prow/jenkins:go_default_library",
        "//prow/kube:go_default_library",
        "//prow/pjutil:go_default_library",
    ],
)

go_binary(
    name = "manual-trigger",
    embed = [":go_default_library"],
    importpath = "k8s.io/test-infra/experiment/manual-trigger",
    visibility = ["//visibility:public"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
    visibility = ["//visibility:public"],
)
