workspace(name = "rules_python_demo")

load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
load("@bazel_tools//tools/build_defs/repo:git.bzl", "new_git_repository")

rules_python_version = "83d404082f2eed11c394fd451943fb0c4586ffa3"

http_archive(
    name = "rules_python",
    url = "https://github.com/AutomatedTester/rules_python/archive/{version}.tar.gz".format(version = rules_python_version),
    strip_prefix = "rules_python-{version}".format(version = rules_python_version),
    sha256 = "0859abbf5759f7b15f2c3a4ccf829abdf5907dfddb88a8ba1299709734af5276",
)

load("@rules_python//python:pip.bzl", "pip_install")

pip_install(
   name = "pypi",
   requirements = "//:requirements.txt",
)

