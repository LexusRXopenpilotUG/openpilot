# Lexus RX openpilot User Group openpilot

This is a repository to store slightly modified forks that are minorly tweaked
for Lexus RX openpilot users that can't be upstreamed.

* [Low-gear/high-RPM on highways with openpilot longitudinal control][ghopissue]
  * openpilot is most useful on highways and it is ironic that it is crippled
    with low fuel milage.
  * The comma team is not willing to split out the DBC for Toyota vehicles so a
    different scaling value can be used.
  * A proposal to have different scaling values for models of vehicles in the
    codebase was not recieved well and called a "hack".
  * No one has or is currently willing to put in the work to try to figure out
    an alternative to stop this gearing issue.
  * The commaai OP team was not going to address this for any vehicles
    pre-TSS2 vehicles such as those using SDSUs. If a solution was presented, it
    might not be backported.

## Prepatched forks available

Prepatched versions of these forks are available at this repository underneath
these branches.

* Stock Comma Release 2 (Stable)
  * `commaai_release2`
* Shane's Stock Additions
  * `shanesmiskol_stock_additions`

## Usage

Please see this Wiki entry. and consider this repository as another fork:

https://github.com/commaai/openpilot/wiki/Forks

If you are not familiar with SSH, you are strongly recommended to use
[Shane's Fork Installer][shaneforkinstaller]. Uninstall openpilot to see the
installation prompt again.

Shane's Fork Installer Example URLs:

* https://smiskol.com/fork/LexusRXopenpilotUG/commaai-release2
* https://smiskol.com/fork/LexusRXopenpilotUG/shanesmiskol-stock_additions

## Behind the Scenes

Please look at the `.github/workflows` repository to see how the pre-patched
branches are updated daily.


[ghopissue]: https://github.com/commaai/openpilot/issues/2106
[shaneforkinstaller]: https://github.com/ShaneSmiskol/openpilot-installer-generator
