# Lexus RX openpilot User Group openpilot

This is a repository to store and continually generate slightly modified forks
that can't be upstreamed and are minorly tweaked for Lexus RX openpilot users.

* [openpilot issue #2106: Low-gear/high-RPM on highways with openpilot longitudinal control][ghopissue]
  * openpilot is most useful on highways and it is ironic that it is crippled
    with low fuel mileage.
  * The comma team does not seem willing to split out the DBC for Toyota
    vehicles so a different scaling value for cruising speed can be used.
  * A proposal to have different scaling values for models of vehicles in the
    codebase while preserving the DBC scaling was not received well and called
    a "hack".
  * No one has or is currently willing to put in the work to try to figure out
    another "proper" alternative to stop this gearing issue.
  * The comma.ai OP team was not going to address this for any vehicles pre-TSS2
    vehicles such as those using SDSUs. If a solution was only usable on TSS2,
    it might not be backported.
  * **PATCH NOTES**
    * Hack vCruise in controlsd.py to scale by 0.974 as soon as possible before
      passing onto rest of openpilot.

## Available Prepatched Forks

Pre-patched versions of these forks are available at this repository underneath
these branches. These are continuously synced daily.


* [Comma.ai Branches (see this link for description)][commaaiext]:
  * "`release2`" (Latest Prebuilt Stable Version for Comma 2)
    * Generated: `commaai_release2`
      * Upstream: https://github.com/commaai/openpilot/tree/release2
  * "`release3`" (Latest Prebuilt Stable Version for Comma 3)
    * Generated: `commaai_release3`
      * Upstream: https://github.com/commaai/openpilot/tree/release3
  * "`release2-staging`"
    * Generated: `commaai_release2-staging`
      * Upstream: https://github.com/commaai/openpilot/tree/release2-staging
  * "`release3-staging`"
    * Generated: `commaai_release3-staging`
      * Upstream: https://github.com/commaai/openpilot/tree/release3-staging
  * "`devel-staging`"
    * Generated: `commaai_devel-staging`
      * Upstream: https://github.com/commaai/openpilot/tree/devel-staging
  * "`devel`"
    * Generated: `commaai_devel-staging`
      * Upstream: https://github.com/commaai/openpilot/tree/devel
  * "`master-ci`"
    * Generated: `commaai_master-ci`
      * Upstream: https://github.com/commaai/openpilot/tree/master-ci
* Shane  
  * SA-master (based on OP 0.8.7)
    * Generated: `shanesmiskol_SA-master`
      * Upstream: https://github.com/ShaneSmiskol/openpilot/tree/SA-master

More forks/branches can be tracked upon request!

## Usage

Please see this wiki entry and consider this repository as another fork:

https://github.com/commaai/openpilot/wiki/Forks

If you are not familiar with SSH or Git, you are recommended to use
[Shane's Fork Installer][shaneforkinstaller]. Uninstall openpilot to see the
installation setup again.

Shane's Fork Installer Example Custom Software Installer URLs:

* https://smiskol.com/fork/LexusRXopenpilotUG/commaai_release2
* https://smiskol.com/fork/LexusRXopenpilotUG/commaai_release3
* https://smiskol.com/fork/LexusRXopenpilotUG/shanesmiskol_SA-master

The updater may or may not work. If it doesn't update, just uninstall and
reinstall with the appropiate above URL.

## Behind the Scenes

Please look at the `.github/workflows` path in this repo to see how the
pre-patched branches are continually updated daily.


[ghopissue]: https://github.com/commaai/openpilot/issues/2106
[shaneforkinstaller]: https://github.com/ShaneSmiskol/openpilot-installer-generator
[commaaiext]: https://comma-ai.medium.com/a-2020-theme-externalization-13b33326d8b3
