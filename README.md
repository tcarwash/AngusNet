AngusNET Experimental Packet Radio Network

Participants

  * Tyler Riddle KG7OEM
  * Jeff Baitis AG7EW
  * Tyler Carr KI7IQE


HOWTO

You'll need these packages for Debian based systems:

  ax25-apps ax25-tools libfile-slurp-perl libyaml-perl
  libipc-system-simple-perl
  cowsay bsdgames animals libfile-slurp-perl telnetd

You'll need these packages from CPAN

  Net::IPAddress::Filter

You'll need a TNC or some form of software modem

  direwolf

In Debian direwolf needs to be compiled if you need hamlib
https://github.com/wb2osz/direwolf

Steps
  # Install the debian packages then install the CPAN packages.
  # Run ./bin/install
  # Run ./bin/update-hosts networks/*
  # Put your AMPR ip address in /etc/local/angusnet/ampr-address on a single line
  # Run systemctl daemon-reload && systemctl enable angusnet-route-fixd && systemctl start angusnet-route-fixd
  # Configure /etc/ax25/axports
  # Create a direwolf configuration in /etc/local/angusnet/direwolf.conf
  # Copy example/direwolf.service to /etc/systemd/system/
  # Configure /etc/systemd/system/direwolf.service
  # Run systemctl daemon-reload
  # Run systemctl start direwolf
