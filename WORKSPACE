workspace(name="org_iota_hub")

# EXTERNAL RULES
git_repository(
    name="org_pubref_rules_protobuf",
    remote="https://github.com/pubref/rules_protobuf",
    tag="v0.8.2")
http_archive(
    name="io_bazel_rules_go",
    url=
    "https://github.com/bazelbuild/rules_go/releases/download/0.11.0/rules_go-0.11.0.tar.gz",
    sha256="f70c35a8c779bb92f7521ecb5a1c6604e9c3edd431e50b6376d7497abc8ad3c1",
)
git_repository(
    name="com_github_nelhage_rules_boost",
    commit="69e96e724cbe746f63d993fa8f6bf772e1ebc5cc",
    remote="https://github.com/nelhage/rules_boost", )

# DEPENDENCIES
git_repository(
    name="com_github_gflags_gflags",
    commit="e292e0452fcfd5a8ae055b59052fc041cbab4abf",
    remote="https://github.com/gflags/gflags.git")
git_repository(
    name="com_github_google_glog",
    commit="2f493d292c92abf16ebd46cfd0cc0bf8eef5724d",
    remote="https://github.com/google/glog.git")
git_repository(
    name="com_google_googletest",
    commit="a6f06bf2fd3b832822cd4e9e554b7d47f32ec084",
    remote="https://github.com/google/googletest.git")

new_git_repository(
    name="hinnant_date",
    remote="https://github.com/HowardHinnant/date.git",
    commit="e5c69d84ab5db3e06170b8eedec1d87841c7fb22",
    build_file="BUILD.date")

new_git_repository(
    name="sqlpp11",
    remote="https://github.com/rbock/sqlpp11.git",
    commit="9d64a5c7411f84cad1da71b23118634b5a62a063",
    build_file="BUILD.sqlpp11")

new_git_repository(
    name="sqlpp11sqlite",
    remote="https://github.com/rbock/sqlpp11-connector-sqlite3.git",
    commit="8d4ea283fa891c3f1eb7e45d012bdd4c0838e13a",
    build_file="BUILD.sqlpp11sqlite")

new_http_archive(
    name="argon2",
    url="https://github.com/P-H-C/phc-winner-argon2/archive/20171227.tar.gz",
    sha256="eaea0172c1f4ee4550d1b6c9ce01aab8d1ab66b4207776aa67991eb5872fdcd8",
    strip_prefix="phc-winner-argon2-20171227",
    build_file="BUILD.argon2"
)

new_http_archive(
    name="sqlite3",
    url="https://www.sqlite.org/2018/sqlite-amalgamation-3230100.zip",
    sha256="4239a1f69e5721d07d9a374eb84d594225229e54be4ee628da2995f4315d8dfc",
    strip_prefix="sqlite-amalgamation-3230100",
    build_file="BUILD.sqlite3"
)

git_repository(
    name="rules_iota",
    remote="https://gitlab.com/iota-foundation/software/rules_iota.git",
    commit="5622593910361262b248ad165aaf60bc87d0fa16")


http_archive(
    name="org_iota_entangled",
    url="https://gitlab.com/iota-foundation/software/entangled/-/archive/develop/entangled-develop.tar.gz",
    strip_prefix="entangled-develop"
)

new_http_archive(
        name="keccak",
        url=
        "https://github.com/gvanas/KeccakCodePackage/archive/c737139c81fd191699886a9a74d3220f6e300b29.zip",
        strip_prefix=
        "KeccakCodePackage-c737139c81fd191699886a9a74d3220f6e300b29",
        build_file="@rules_iota//:build/BUILD.keccak",
        sha256=
        "35c63620721ac4da418d4bb427ba7ae9aae76b4a1bea7758d6694a29f6e6488a")


load("@com_github_nelhage_rules_boost//:boost/boost.bzl", "boost_deps")
load("@org_pubref_rules_protobuf//cpp:rules.bzl", "cpp_proto_repositories")
load("@io_bazel_rules_go//go:def.bzl", "go_rules_dependencies",
     "go_register_toolchains", "go_prefix")
load("@org_pubref_rules_protobuf//go:rules.bzl", "go_proto_repositories")
load("@org_pubref_rules_protobuf//grpc_gateway:rules.bzl",
     "grpc_gateway_proto_repositories")

boost_deps()
cpp_proto_repositories()
go_rules_dependencies()
go_register_toolchains()
go_proto_repositories()
grpc_gateway_proto_repositories()
