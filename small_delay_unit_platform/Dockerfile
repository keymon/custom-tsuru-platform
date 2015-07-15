from	ubuntu:14.04
# Create a fake tsuru_unit_agent
run echo "#!/bin/sh\nsleep 31" > /usr/local/bin/tsuru_unit_agent
run	chmod +x /usr/local/bin/tsuru_unit_agent
# Add the ubuntu user
useradd -m ubuntu -s /bin/bash
echo "ubuntu ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
