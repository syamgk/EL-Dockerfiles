FROM registry.access.redhat.com/rhel7

# https://copr.fedorainfracloud.org/coprs/jpopelka/mercator/
# https://copr.fedorainfracloud.org/coprs/fche/pcp/
COPY hack/_copr_jpopelka-mercator.repo hack/_copr_fche_pcp.repo /etc/yum.repos.d/

# Install RPM dependencies
COPY hack/install_deps_rpm.sh /tmp/install_deps/
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
    /tmp/install_deps/install_deps_rpm.sh && \
    yum clean all
