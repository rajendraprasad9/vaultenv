load("@io_tweag_rules_haskell//haskell:haskell.bzl", "haskell_library")

haskell_library(
  name = "free",
  # Normally we prefer to avoid setting the version in a library definition,
  # because it makes the build definition less portable. For many updates, the
  # build definition does not need to be changed, specifying the version causes
  # unnecessary churn. But for "free", the lens package depends on it and uses
  # a MIN_VERSION_free macro for conditional compilation. So in this case we do
  # need an accurate version.
  version = "4.12.4",
  visibility = ["//visibility:public"],
  deps = [
    "@hackage_semigroupoids//:semigroupoids",
    "@hackage_exceptions//:exceptions",
    "@hackage_comonad//:comonad",
    "@hackage_distributive//:distributive",
    "@hackage_semigroups//:semigroups",
    "@hackage_bifunctors//:bifunctors",
    "@hackage_mtl//:mtl",
    "@hackage_prelude_extras//:prelude-extras",
    "@hackage_transformers_compat//:transformers-compat",
    "@hackage_profunctors//:profunctors",
  ],
  prebuilt_dependencies = [
    "base",
    "containers",
    "transformers",
    "template-haskell",
  ],
  srcs = [
    "src/Control/Alternative/Free.hs",
    "src/Control/Alternative/Free/Final.hs",
    "src/Control/Applicative/Free.hs",
    "src/Control/Applicative/Free/Final.hs",
    "src/Control/Applicative/Trans/Free.hs",
    "src/Control/Comonad/Cofree.hs",
    "src/Control/Comonad/Cofree/Class.hs",
    "src/Control/Comonad/Trans/Cofree.hs",
    "src/Control/Comonad/Trans/Coiter.hs",
    "src/Control/Monad/Free.hs",
    "src/Control/Monad/Free/Church.hs",
    "src/Control/Monad/Free/Class.hs",
    "src/Control/Monad/Free/TH.hs",
    "src/Control/Monad/Trans/Free.hs",
    "src/Control/Monad/Trans/Iter.hs",
    "src/Control/Monad/Trans/Free/Church.hs",
  ],
  src_strip_prefix = "src",
)