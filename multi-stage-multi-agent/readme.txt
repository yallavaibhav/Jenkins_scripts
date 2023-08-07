What if you have a 3-tier application where you have a front end, backend and Database.
Here the front and back end might be using Ubuntu, and the database is using centos. 

For this if we use the VMs then it is fine but we cant auto scale (without tools). Secondly, for one VM (Jenkins slave) one team needs python 3.7 and other team needs Python 3.10. For this we need to recongifure the VM based on the teams requirments. 

Instead if we use docker multi-stage, we can easily change the versions by just changig the script from python 3.7 to 3.10. (2 second work)

And once the script is done, that is all the stages such as test, build etc are completed then it will delete the conytaoiner without wasting the resources.
