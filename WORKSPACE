workspace(name = "com_github_zaucy_dca")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
http_archive(
    name = "io_bazel_rules_go",
    urls = [
        "https://storage.googleapis.com/bazel-mirror/github.com/bazelbuild/rules_go/releases/download/0.18.6/rules_go-0.18.6.tar.gz",
        "https://github.com/bazelbuild/rules_go/releases/download/0.18.6/rules_go-0.18.6.tar.gz",
    ],
    sha256 = "f04d2373bcaf8aa09bccb08a98a57e721306c8f6043a2a0ee610fd6853dcde3d",
)
load("@io_bazel_rules_go//go:deps.bzl", "go_rules_dependencies", "go_register_toolchains")
go_rules_dependencies()
go_register_toolchains()

# Download Gazelle
http_archive(
    name = "bazel_gazelle",
    urls = ["https://github.com/bazelbuild/bazel-gazelle/releases/download/0.17.0/bazel-gazelle-0.17.0.tar.gz"],
    sha256 = "3c681998538231a2d24d0c07ed5a7658cb72bfb5fd4bf9911157c0e9ac6a2687",
)

# Load and call Gazelle dependencies
load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")
gazelle_dependencies()

go_repository(
  name = "com_github_jonas747_ogg",
  importpath = "github.com/jonas747/ogg",
  commit = "b4f6f4cf3757a3bf88eae9222045b99b9d76d8ca",
)

go_repository(
  name = "com_github_bwmarrin_discordgo",
  importpath = "github.com/bwmarrin/discordgo",
  tag = "v0.19.0",
)

go_repository(
  name = "org_golang_x_crypto",
  importpath = "golang.org/x/crypto",
  commit = "4def268fd1a49955bfb3dda92fe3db4f924f2285",
)

go_repository(
  name = "com_github_gorilla_websocket",
  importpath = "github.com/gorilla/websocket",
  tag = "v1.4.0",
)
