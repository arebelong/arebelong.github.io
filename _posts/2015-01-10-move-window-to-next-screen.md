http://askubuntu.com/questions/22207/quickly-place-a-window-to-another-screen-using-only-the-keyboard



    Install CompizConfig Settings Manager Install compizconfig-settings-manager

    apt-get install compizconfig-settings-manager

    Run it → Go to bottom (Window Management) → Go to "Put."
    Enable the plugin.
    Configure shortcut for "Put to next Output."
    Log out and back in again.

If the plugin put doesn't appear in CCSM, install the compiz-plugins Install compiz-plugins package. (sudo apt-get update && sudo apt-get install compiz-plugins)

EDIT: The required plugin package is now called compiz-plugins on 12.10 and higher. compiz-plugins-extra Install compiz-plugins-extra is still used for 12.04.

