# My Custom Scripts
There are scripts that I use in places like slstatus. For volume and brightness, if using sxhkd with slstatus, I use this:

	# Volume
	{XF86AudioMute,XF86AudioRaiseVolume,XF86AudioLowerVolume}
		amixer sset Master {toggle,5%+,5%-}; pkill -SIGUSR1 slstatus

	# Backlight
	{XF86MonBrightnessUp,XF86MonBrightnessDown}
		xbacklight -{inc,dec} 10; pkill -SIGUSR1 slstatus

That way it updates instantly.
