# Adding and organizing Groups

As you add more Test Configurations, it makes sense to create a hierarchy in which to organize them, a bit like this.

![](test-manager.png)

There are two ways in which you can do this.

<img src="connecting-groups.png" alt="connecting groups" width="300"/>

- **Add subgroup button** : If you hover over a Group, you will see a button appear **Add a subgroup**. If you press, this, a new group is created and connected.

- **Manually connect** : You can also manually connect an orphaned Group or a hierarchy of Groups whose top Group is not already connected. If you hover over a Group, a connector dot will appear at the bottom of the Group. Click and drag from this dot to the child Group to connect.


## Where Groups and Test Configurations are stored
All Vizitest configuration data is stored in the ```.vizitest``` folder in the root of your codebase.

The folder structure within this mirrors the structure of your project's Groups. Test Configurations are stored within folders.

<warning>
    <p>
        You should be very careful when modifying the structure and contents. You are likely to break the Test Manager if you do so. 
    </p>
    <p>
        Generally speaking there is no reason to do so as it's all managed by Vizitest.
    </p>
</warning>
