#
# Copyright IBM Corp. All Rights Reserved.
#
# SPDX-License-Identifier: Apache-2.0
#

# Use the same docker image that is used as the hyperledger base image
FROM hyperledger/fabric-basejvm:x86_64-0.3.2-snapshot-1d0fa6d

RUN mkdir -p /tmp/scripts
COPY scripts /tmp/scripts
RUN cd /tmp/scripts && \
    init.sh && \
    rm -rf /tmp/scripts
ENV GOPATH=/opt/gopath
ENV GOROOT=/opt/go
ENV PATH=$PATH:$GOROOT/bin:$GOPATH/bin
