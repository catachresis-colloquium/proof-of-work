# SPDX-License-Identifier: MPL-2.0
#
# Named `Dockerfile`, not `Containerfile`, on purpose. ClusterFuzzLite's
# build_fuzzers action runs `docker build -f .clusterfuzzlite/Dockerfile` and
# has no input to change the name. The estate's "use Containerfile" rule (root
# probes in contractile.just and Trustfile.a2ml) is about the repo root. This
# file was renamed by an auto-sync in acd848f, and every ClusterFuzzLite run
# failed from then on with "open Dockerfile: no such file or directory".
FROM gcr.io/oss-fuzz-base/base-builder-rust

COPY . $SRC/proof-of-work
WORKDIR $SRC/proof-of-work

COPY .clusterfuzzlite/build.sh $SRC/
