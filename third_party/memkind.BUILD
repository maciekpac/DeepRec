package(default_visibility = ["//visibility:public"])

licenses(["restricted"])  # GNU General Public License ("GPL") version 2


load("@rules_cc//cc:defs.bzl", "cc_test")
load("@rules_foreign_cc//foreign_cc:defs.bzl", "configure_make")


filegroup(
    name = "all",
    srcs = glob(
        include=[
            "**"
        ],
    ),
)

configure_make(
    name = "memkind",
    lib_source = "//:all",
    configure_in_place = True,
    autogen = True,
    out_static_libs = [
        "libmemkind.a"
    ],
    visibility = [ "//visibility:public" ],
)
