default: help
.PHONY: default

help:
	@echo 'Usage:'
	@echo '	$$ make [action]'
	@echo
	@echo 'Example:'
	@echo '	$$ make'
	@echo '	$$ make help'
	@echo
	@echo '	$$ make clone'
	@echo
	@echo '	$$ make prepare-arch-build'
	@echo
	@echo '	$$ make prepare-debian-build'
	@echo
	@echo '	$$ make build'
	@echo
	@echo '	$$ make clean'
	@echo
	@echo '	$$ make install'
	@echo
	@echo '	$$ make remove'
	@echo

.PHONY: help


install: qpwm-install xsession-install config-install
.PHONY: install

remove: qpwm-remove xsession-remove config-remove
.PHONY: remove




##
## * https://github.com/ssleert/qpwm
##

prepare-debian-build:
	sudo apt-get install gcc make libx11-dev git
.PHONY: prepare-debian-build

prepare-arch-build:
	sudo pacman -Sy --needed gcc make libx11 git
.PHONY: prepare-arch-build




clone:
	git clone https://github.com/ssleert/qpwm.git src/qpwm
.PHONY: clone




build:
	cp -a asset/overlay/qpwm/config.h src/qpwm/config.h
	make -C src/qpwm
.PHONY: build

clean:
	make -C src/qpwm clean
.PHONY: clean


qpwm-install: build
#	sudo install -Dm755 ./src/qpwm/qpwm /usr/bin/qpwm
	sudo install -Dm755 ./src/qpwm/qpwm /usr/local/bin/qpwm
.PHONY: qpwm-install

qpwm-remove:
#	sudo rm -f /usr/bin/qpwm
	sudo rm -f /usr/local/bin/qpwm
.PHONY: qpwm-remove




xsession-install:
	make -C ./asset/xsession install
.PHONY: xsession-install

xsession-remove:
	make -C ./asset/xsession remove
.PHONY: xsession-remove




config-install:
	make -C ./asset/config install
.PHONY: config-install

config-remove:
	make -C ./asset/config remove
.PHONY: config-remove
