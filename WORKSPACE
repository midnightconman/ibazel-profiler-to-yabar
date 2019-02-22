
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "io_bazel_rules_go",
    urls = ["https://github.com/bazelbuild/rules_go/releases/download/0.17.0/rules_go-0.17.0.tar.gz"],
    sha256 = "492c3ac68ed9dcf527a07e6a1b2dcbf199c6bf8b35517951467ac32e421c06c1",
)

http_archive(
    name = "bazel_gazelle",
    urls = ["https://github.com/bazelbuild/bazel-gazelle/releases/download/0.16.0/bazel-gazelle-0.16.0.tar.gz"],
    sha256 = "7949fc6cc17b5b191103e97481cf8889217263acf52e00b560683413af204fcb",
)

load("@io_bazel_rules_go//go:deps.bzl", "go_rules_dependencies", "go_register_toolchains")

go_rules_dependencies()
go_register_toolchains()

load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")

gazelle_dependencies()

# external dependencies

go_repository(
    name = "org_golang_x_crypto",
    commit = "0c41d7ab0a0e",
    importpath = "golang.org/x/crypto",
)

go_repository(
    name = "org_golang_x_sys",
    commit = "8469e314837c",
    importpath = "golang.org/x/sys",
)

go_repository(
    name = "com_github_fsnotify_fsnotify",
    commit = "ccc981bf80385c528a65fbfdd49bf2d8da22aa23",
    importpath = "github.com/fsnotify/fsnotify",
)

go_repository(
    name = "com_github_sirupsen_logrus",
    commit = "4f5fd631f16452fbd023813c1eb7dbd67130cb0c",
    importpath = "github.com/sirupsen/logrus",
)
