# How to

![infra instance with multiple network](./img/03-multiple-network.png "infra instance with multiple network")

### Create stack

```
terraform apply
```

This script will create:
-   1 vpc
-   2 networks
-   2 instances http
-   3 instances db

### Delete stack

```
terraform destroy
```

### Creating a New Environment
1. Create a new branch (git branch) for the environment you wish to set up.
2. Add the necessary context to the CircleCI configuration file by creating a new context with the same name as the branch you created.
3. Modify the CircleCI configuration to include a filter for the new branch. This will ensure that the pipeline is triggered only when changes are made to this specific branch.
4. The context you created in step 2 should modify the prefixes of the instance names.

For example, if you created a branch called test, and the context associated with this branch is configured to modify the prefixes, the HTTP instance name could be changed from http-instance to test-http-instance, and the database instance name could be changed from db-instance to test-db-instance.

By following these steps, you will be able to create new environments easily and efficiently. Good luck with your work!
