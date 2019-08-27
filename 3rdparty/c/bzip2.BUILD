package(default_visibility = ["//visibility:public"])

cc_library(
    name = "bz2",
    srcs = [
        "blocksort.c",
        "bzlib.c",
        "compress.c",
        "crctable.c",
        "decompress.c",
        "huffman.c",
        "randtable.c",
    ],
    hdrs = [
        "bzlib.h",
        "bzlib_private.h",
    ],
    includes = [
        ".",
    ],
)

cc_library(
    name = "libbz2",
    # Import `:bz2` as `srcs` to enforce the library name `libbz2.so`.
    # Otherwise, Bazel would mangle the library name and e.g. Cabal wouldn't
    # recognize it.
    srcs = [":bz2"],
    hdrs = [
        "bzlib.h",
        "bzlib_private.h",
    ],
    includes = [
        ".",
    ],
    visibility = [
        "//visibility:public",
    ],
)
