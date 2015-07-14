from	ubuntu:14.04
run	apt-get update
run	apt-get install wget -y --force-yes
# Install the base files
run	wget http://github.com/tsuru/basebuilder/tarball/master -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	/var/lib/tsuru/base/install
# Start script
run cp /var/lib/tsuru/base/start /var/lib/tsuru
# Deploy script
run wget https://raw.githubusercontent.com/keymon/custom-tsuru-platform/master/delay_unit_platform/deploy -O /var/lib/tsuru/deploy --no-check-certificate
run	chmod +x /var/lib/tsuru/deploy
# Deploy script
run wget https://raw.githubusercontent.com/keymon/custom-tsuru-platform/master/delay_unit_platform/Procfile -O /var/lib/tsuru/utils/Procfile --no-check-certificate
# Replace the original tsuru_unit_agent
run mv /usr/local/bin/tsuru_unit_agent /usr/local/bin/orig_tsuru_unit_agent
run wget https://raw.githubusercontent.com/keymon/custom-tsuru-platform/master/delay_unit_platform/delay_tsuru_unit_agent -O /usr/local/bin/tsuru_unit_agent --no-check-certificate
run	chmod +x /usr/local/bin/tsuru_unit_agent

