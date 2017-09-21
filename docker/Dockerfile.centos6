FROM centos:6
RUN yum install -y centos-release-scl
RUN yum install -y cmake devtoolset-6-gcc devtoolset-6-gcc-c++ devtoolset-6-make ImageMagick-c++-devel ImageMagick-devel doxygen ruby193 ruby193-ruby-devel rpm-build
RUN scl enable devtoolset-6 ruby193 bash
ENV PERL5LIB=/opt/rh/devtoolset-6/root//usr/lib64/perl5/vendor_perl:/opt/rh/devtoolset-6/root/usr/lib/perl5:/opt/rh/devtoolset-6/root//usr/share/perl5/vendor_perl \
  LD_LIBRARY_PATH=/opt/rh/devtoolset-6/root/usr/lib64:/opt/rh/devtoolset-6/root/usr/lib:/opt/rh/ruby193/root/usr/lib64 \
  PATH=/opt/rh/devtoolset-6/root/usr/bin:/opt/rh/ruby193/root/usr/bin:/opt/rh/ruby193/root/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin \
  PYTHONPATH=/opt/rh/devtoolset-6/root/usr/lib64/python2.6/site-packages:/opt/rh/devtoolset-6/root/usr/lib/python2.6/site-packages \
  PKG_CONFIG_PATH=/opt/rh/ruby193/root/usr/lib64/pkgconfig
RUN gem install --no-ri --no-rdoc package_cloud fpm
