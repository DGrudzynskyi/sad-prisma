Files/utils, not being a part of original `prisma` reporitory.
Used for local harness and experiments.

In order to create a docker-packed prisma instance do this:
- install openjdk@8
- install sbt
- from the `../server` folder:
- `sbt update`
- `source .envrc`
- `sbt "project prisma-local" docker` - image is built but not named. Can't find the sbt-docker package compatible with both old java/scala and fresh docker.
- rename anonymous image `docker tag {whateverTagIsAutoAssigned} {whateverNameYouWantToGiveToDockerImage}`