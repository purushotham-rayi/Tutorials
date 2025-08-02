# Setup Questions

1. Can I bind two host volumes to a single docker container?
- No, you cannot. You can only mount one bind volume.
2. How to save data of two separate apps in a single mongodb image MongoDB image?
- Just save it to two different databases. MongoDB allows all the data to be saved to /data/db folder only. If you need complete isolation between the two projects, create two separate containers for each.
3. What about Spark. Can we save output files of two projects in two separate folders?
    ### Two separate Docker compose files
    - Create two separate containers using docker compose.
    - Map the host volumes separately with respective folders where you wish to save the files using bind mounts.
    - Complete isolation from each other.
    ### Single docker compose files but spin up up two spark clusters.
    - Essentially works the same way as the above one. But we launch two containers in the same file for both the spark clusters.
    - We mount the host storage location using their respective folders.
    - All containers start from a single docker compose file and can be managed together. This is the only difference from the first approach.
    ### Shared Spark cluster
    - Applications share resources from the same Spark clusters.
    - You can mount both the folders to the same cluster.
    - Spark automatically shares resources between the two applications. Writing to the required destination can be configured using the spark code.
    - Use this when you create the multi-device setup. Will be useful for resource sharing.