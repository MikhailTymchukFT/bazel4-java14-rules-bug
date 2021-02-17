load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive", "http_file")

http_archive(
    name = "remote_java_tools_darwin",
    sha256 = "ceebee0618e838a0aa904f010e382a407e4ef6302d5d35c803e77b29612c3224",
    urls = [
            "https://mirror.bazel.build/bazel_java_tools/releases/javac14/v2.0/java_tools_javac14_darwin-v2.0.zip",
            "https://github.com/bazelbuild/java_tools/releases/download/javac14_v2.0/java_tools_javac14_darwin-v2.0.zip",
        ],
)

http_archive(
    name = "openjdk8u242_darwin_archive",
    build_file_content = """
package(default_visibility = ["//visibility:public"])

java_runtime(
    name = 'runtime',
    srcs =  glob(['**']),
    java='//:Contents/Home/bin/java'
)
""",
    sha256 = "06675b7d65bce0313ee1f2e888dd44267e8afeced75e0b39b5ad1f5fdff54e0b",
    strip_prefix = "jdk8u242-b08",
    urls = ["https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_x64_mac_hotspot_8u242b08.tar.gz"],
)
