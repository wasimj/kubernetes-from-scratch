<!---
    Start up vagrant and connect to master node
-->

vagrant up

vagrant ssh master

sudo su

<!---
    Then run package installation on master
    Run each command sequentially. Running the shell script as a whole won't work.
    0-PackageInstallation.sh
-->
