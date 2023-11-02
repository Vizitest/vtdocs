# Adding and organizing Groups

As you add more Test Configurations, it makes sense to create a hierarchy in which to organize them.

Groups are the main containers you will find on the canvas. Within a Group is a list of Test Configurations.

## Add a Group
There are two ways to add a Group.

- **Add subgroup** button : If you hover over a Group, you will see a button appear **Add a subgroup**. If you press, this, a new group is created and connected.

<img src="connecting-groups.png" alt="connecting groups" width="300"/>

- **Add an orphaned Group** : press the large, blue **+** button in the top left of the canvas.

<img src="test-manager.png" alt="add group" width="600"/>

## Connecting Groups
If you used the **Add subgroup** button, the Groups will already be connected.

If you have an orphaned Group that you want to make a child of another Group, then you can connect it manually.

- Hover over a Group.
- A connector dot will appear at the bottom of the Group.
- Click and drag from this dot to the dot at the top of the orphaned Group you want to make its child.

You should now see the connecting line.

## Deleting a Connector
You can remove the parent/child connector by hovering on the connector and then pressing the X button that appears in the midpoint of the line.

<img src="remove-connector.png" alt="delete connector" width="300"/>

## Deleting a Group
You can delete a Group, without deleting its children, [as explained here](group-delete.md).

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
