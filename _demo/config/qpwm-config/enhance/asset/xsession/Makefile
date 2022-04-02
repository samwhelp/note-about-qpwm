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
	@echo '	$$ make install'
	@echo
	@echo '	$$ make remove'
	@echo

.PHONY: help


install: xsession-install config-install
.PHONY: install

xsession-install:
	sudo install -Dm644 ./xsessions/qpwm-session.desktop /usr/share/xsessions/qpwm-session.desktop
	sudo install -Dm755 ./xsessions/qpwm-session /usr/share/qpwm/xsessions/qpwm-session
.PHONY: xsession-install

config-install:
	sudo install -Dm644 ./config/qpwm/environment /usr/share/qpwm/config/qpwm/environment
	sudo install -Dm755 ./config/qpwm/autostart /usr/share/qpwm/config/qpwm/autostart
.PHONY: config-install




remove: xsession-remove config-remove
.PHONY: remove

xsession-remove:
	sudo rm -f /usr/share/xsessions/qpwm-session.desktop
	sudo rm -f /usr/share/qpwm/xsessions/qpwm-session
.PHONY: xsession-remove

config-remove:
	sudo rm -f /usr/share/qpwm/config/qpwm/environment
	sudo rm -f /usr/share/qpwm/config/qpwm/autostart
.PHONY: config-remove
