package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "doc.go",
        "registry.go",
        "strategy.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/rest:go_default_library",
        "//pkg/apis/extensions:go_default_library",
        "//pkg/apis/extensions/validation:go_default_library",
        "//pkg/controller/deployment/util:go_default_library",
        "//pkg/fields:go_default_library",
        "//pkg/genericapiserver/api/request:go_default_library",
        "//pkg/registry/generic:go_default_library",
        "//pkg/storage:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/labels",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/validation/field",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["strategy_test.go"],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/testapi:go_default_library",
        "//pkg/api/testing:go_default_library",
        "//pkg/apis/extensions:go_default_library",
        "//pkg/genericapiserver/api/request:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//pkg/registry/extensions/deployment/storage:all-srcs",
    ],
    tags = ["automanaged"],
)
