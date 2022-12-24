load("@rules_d//d:d.bzl", "d_binary", "d_docs", "d_library", "d_source_library", "d_test")

lmdbd_imports = ["source"]

d_library(
    name = "lmdbd",
    srcs = [
		"source/lmdb/binding.d",
		"source/lmdb/macros.d",
	],
	deps = ["@lmdb//:lmdb"],
	imports = lmdbd_imports,
)

d_test(
	name = "lmdbd_test",
	srcs = ["source/lmdb/package.d"],
	deps = [":lmdbd"],
	imports = lmdbd_imports,
)

d_docs(
	name = "lmdbd_docs",
	dep = ":lmdbd",
)
