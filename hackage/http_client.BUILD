load("@io_tweag_rules_haskell//haskell:haskell.bzl", "haskell_library")

haskell_library(
  name = "public_suffix_list",
  deps = [
    "@hackage_text//:text",
    "@hackage_blaze_builder//:blaze-builder",
  ],
  prebuilt_dependencies = [
    "base",
    "containers",
  ],
  srcs = [
    "publicsuffixlist/Network/PublicSuffixList/DataStructure.hs",
    "publicsuffixlist/Network/PublicSuffixList/Lookup.hs",
    "publicsuffixlist/Network/PublicSuffixList/Serialize.hs",
    "publicsuffixlist/Network/PublicSuffixList/Types.hs",
  ],
  src_strip_prefix = "publicsuffixlist",
)

haskell_library(
  name = "http-client",
  visibility = ["//visibility:public"],
  deps = [
    ":public_suffix_list",
    "@hackage_cookie//:cookie",
    "@hackage_exceptions//:exceptions",
    "@hackage_streaming_commons//:streaming-commons",
    "@hackage_case_insensitive//:case-insensitive",
    "@hackage_stm//:stm",
    "@hackage_base64_bytestring//:base64-bytestring",
    "@hackage_text//:text",
    "@hackage_network//:network",
    "@hackage_blaze_builder//:blaze-builder",
    "@hackage_mime_types//:mime-types",
    "@hackage_network_uri//:network-uri",
    "@hackage_random//:random",
    "@hackage_http_types//:http-types",
  ],
  prebuilt_dependencies = [
    "bytestring",
    "base",
    "time",
    "filepath",
    "array",
    "containers",
    "ghc-prim",
    "transformers",
    "deepseq",
  ],
  srcs = [
    "Data/KeyedPool.hs",
    "Network/HTTP/Client.hs",
    "Network/HTTP/Client/MultipartFormData.hs",
    "Network/HTTP/Client/Internal.hs",
    "Network/HTTP/Client/Body.hs",
    "Network/HTTP/Client/Connection.hs",
    "Network/HTTP/Client/Cookies.hs",
    "Network/HTTP/Client/Core.hs",
    "Network/HTTP/Client/Headers.hs",
    "Network/HTTP/Client/Manager.hs",
    "Network/HTTP/Client/Request.hs",
    "Network/HTTP/Client/Response.hs",
    "Network/HTTP/Client/Types.hs",
    "Network/HTTP/Client/Util.hs",
    "Network/HTTP/Proxy.hs",
  ],
)
