licenses(["notice"])

filegroup(
    name = "srcs",
    srcs = glob(["**/**"]),
    visibility = [
        "//visibility:public",
    ],
)

filegroup(
    name = "cc_builtin_test_files",
    srcs = glob(["cc/**/**"]),
)

sh_test(
    name = "cc_builtin_tests",
    size = "medium",
    srcs = ["cc_builtin_tests.sh"],
    data = [
        ":builtin_test_setup",
        ":cc_builtin_test_files",
        "//src/test/shell/bazel:test-deps",
    ],
    tags = ["no_windows"],
)

sh_library(
    name = "builtin_test_setup",
    srcs = ["builtin_test_setup.sh"],
)
