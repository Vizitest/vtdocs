# Vizitest and Git 

All of your Vizitest Projects and their Test Configurations are stored within the codebase itself. This makes it fundamentally compatible with Git. When you push the code repository, you will also be pushing your Vizitest work.

## What about conflicts?
There are specific conflict cases that are worth mentioning.

### Parallel edits to a Test Configuration
It is, by and large, unlikely that two people will be working in parallel on the same Test Configuration. However, it can, and therefore will at some point, happen.

In this situation, a conflict will arise that needs to be resolved.

Test configurations are JSON files. This means that in theory, they can be resolved at a granular level. In practice, however, trying to resolve these if there are several differences, is likely to be more trouble than it's worth. 

In this situation, the most pragmatic solution will often be to just accept one version or the other. 

### Naming of a Test Configuration in a Group
[TODO - Daniel, not sure exactly what but you mentioned a situation where this could happen]

