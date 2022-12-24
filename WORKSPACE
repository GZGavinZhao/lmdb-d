load("@bazel_tools//tools/build_defs/repo:git.bzl", "git_repository")
git_repository(
	name = "rules_d",
	remote = "https://github.com/bazelbuild/rules_d.git",
	commit = "91005313d9789861fb86d4d75fc06c3b45eda903",
)
load("@rules_d//d:d.bzl", "d_repositories")
d_repositories()

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")
http_archive(
	name = "lmdb",
	urls = ["https://github.com/LMDB/lmdb/archive/refs/tags/LMDB_0.9.29.tar.gz"],
	sha256 = "22054926b426c66d8f2bc22071365df6e35f3aacf19ad943bc6167d4cae3bebb",
	strip_prefix = "lmdb-LMDB_0.9.29",
	build_file_content = '''
package(default_visibility = ["//visibility:public"])

cc_library(
	name = "lmdb",
	hdrs = glob(["libraries/liblmdb/*.h"]),
	srcs = [
		"libraries/liblmdb/mdb.c",
		"libraries/liblmdb/midl.c",
	],
	linkopts = ["-pthread"],
)
''',
)
