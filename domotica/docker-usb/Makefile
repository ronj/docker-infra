PREFIX = /usr/local

.PHONY: info install uninstall

info:
	@echo
	@echo "Usage: make [install | uninstall]"
	@echo

install:
	sudo cp ./docker-swarm-usb-listener $(DESTDIR)$(PREFIX)/bin/docker-swarm-usb-listener-start
	sudo cp ./docker-swarm-usb-listener $(DESTDIR)$(PREFIX)/bin/docker-swarm-usb-listener
	sudo cp ./docker-swarm-usb-enable $(DESTDIR)$(PREFIX)/bin/docker-swarm-usb-enable
	sudo cp ./99-libftdi.rules $(DESTDIR)/etc/udev/rules.d/99-libftdi.rules
	sudo cp ./99-zwave.rules $(DESTDIR)/etc/udev/rules.d/99-zwave.rules
	sudo udevadm control --reload-rules
	sudo udevadm trigger

uninstall:
	sudo rm $(DESTDIR)$(PREFIX)/bin/docker-swarm-usb-listener-start
	sudo rm $(DESTDIR)$(PREFIX)/bin/docker-swarm-usb-listener
	sudo rm $(DESTDIR)$(PREFIX)/bin/docker-swarm-usb-enable
	sudo rm $(DESTDIR)/etc/udev/rules.d/99-libftdi.rules
	sudo rm $(DESTDIR)/etc/udev/rules.d/99-zwave.rules
	sudo udevadm control --reload-rules
	sudo udevadm trigger
