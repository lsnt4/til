# Remove `<none>` Tagged Docker Images

### Question:
Accidently when we create Docker images without a tag, sometimes it's not that much easy to remove that particular image. Even we used the `-f` flag, image removal will fail with a warning.

In this case, let's assume that we have an image called `foo-image` without a tag.

```shell
$ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
foo-image           <none>              ed69ee3e546a        2 weeks ago         133.7 MB
```
When we try to force remove it, it will give following error.

```shell
$ docker rmi -f ed69ee3e546a
Error response from daemon: conflict: unable to delete ed69ee3e546a (cannot be forced) - image has dependent child images
```

### Answer:
First add a tag to that image, in this case it's called `bar`.

```shell
$ docker tag ed69ee3e546a foo-image:bar
```
Remove the image as usual with new tag or you should be able to use the image id if you're not sure.
```shell
$ docker rmi foo-image:bar
Untagged: foo-image:bar
Untagged: foo-image@sha256:0bb659eafa22cdb9f14bc05d17be97132842eb122eb8ff346ecafe7553f48f22
```

### Notes:
* You may need root privileges to handle Docker daemon.

### Resources:
[Stack Overflow](http://stackoverflow.com/a/25214186/3683435)
