# top-tar-nn

This project containers a Docker setup for MadGraph with Pythia and Delphes for generating ttbar event samples.

## Usage:
### Docker
On a local machine with Docker installed (e.g. your laptop), execute:
```
mkdir output
docker run -it --rm --volume $PWD/output:/var/MG_outputs --volume /tmp:/tmp philippgadow/top-tar-nn
# ignore warning about groups: cannot find name for group ID 1099333925
```

### Usage of MadGraph inside container
```
# inside the container
mkdir ~/mg5_output
cd ~/mg5_output

# launch mg5 with default event generation for top quark pair production
/home/hep/MG5_aMC_v2_7_3/bin/mg5_aMC /home/hep/commands/generate_sm_ttbar_delphes.cmnd
```
