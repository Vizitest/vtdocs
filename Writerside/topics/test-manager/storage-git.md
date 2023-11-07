# Where Groups and Test Configurations are stored
Vizitest is Git friendly, so use Git to get you out of trouble.

All Vizitest metadata is stored in ```yaml``` and ```json``` files in the ```.vizitest``` folder in the root of your project.

Once you have configured some Groups and Test Configurations, take a look within the ```.vizitest``` folder. You should see

- Root level Groups can be found at the root level as folders.
- Child Groups are sub folders.
- Test Configurations have their own folders as sub folders of the Group folder to which they belong.
- ```yaml``` files contain high level metadata for Groups and Test Configurations
- Test Configurations are stores as ```.tconfig``` files and contain ```json```.

## Working with Git
Because Vizitest stores its data in text files (```yaml``` and ```json```), any conflicts are resolvable. 

A merge conflict should only arise under the following circumstances.

- Two people work on the same Test Configuration and then update changes. In this situation, the best way to resolve the conflict is for a decision to be made which version to accept and then accept all changes. Attempting to resolve conflicts within the json itself is likely to be a major challenge.
- Two people make changes to the Group layout. 
