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
	@echo '	$$ make test'
	@echo

.PHONY: help


install: autostart-install config-install compositor-install panel-install wallpaper-install
#	tree --dirsfirst ~/.config/qpwm
.PHONY: install

autostart-install:
	install -Dm644 ./qpwm/environment ~/.config/qpwm/environment
	install -Dm755 ./qpwm/autostart ~/.config/qpwm/autostart
.PHONY: autostart-install

config-install:
	install -Dm644 ./qpwm/sxhkdrc ~/.config/qpwm/sxhkdrc
.PHONY: config-install

panel-install:
	install -Dm644 ./qpwm/style/tint2/tint2rc ~/.config/qpwm/style/tint2/tint2rc
.PHONY: panel-install

compositor-install:
	install -Dm644 ./qpwm/style/picom/picom.conf ~/.config/qpwm/style/picom/picom.conf
.PHONY: compositor-install

wallpaper-install:
	install -Dm755 ./qpwm/bin/qpwm-wallpaper-ctrl-shuf ~/.config/qpwm/bin/qpwm-wallpaper-ctrl-shuf
	install -Dm755 ./qpwm/bin/qpwm-wallpaper-ctrl-default ~/.config/qpwm/bin/qpwm-wallpaper-ctrl-default
.PHONY: wallpaper-install




remove: autostart-remove config-remove compositor-remove panel-remove wallpaper-remove
#	tree --dirsfirst ~/.config/qpwm
.PHONY: remove

autostart-remove:
	rm -f ~/.config/qpwm/environment
	rm -f ~/.config/qpwm/autostart
.PHONY: autostart-remove

config-remove:
	rm -f ~/.config/qpwm/sxhkdrc
.PHONY: config-remove

panel-remove:
	rm -f  ~/.config/qpwm/style/tint2/tint2rc
.PHONY: panel-remove

compositor-remove:
	rm -f  ~/.config/qpwm/style/picom/picom.conf
.PHONY: compositor-remove

wallpaper-remove:
	rm -f  ~/.config/qpwm/bin/qpwm-wallpaper-ctrl-shuf
	rm -f  ~/.config/qpwm/bin/qpwm-wallpaper-ctrl-default
.PHONY: wallpaper-remove


test:
	./xephyr-run-qpwm.sh
.PHONY: test

stop:
	killall -9 bash
.PHONY: stop
