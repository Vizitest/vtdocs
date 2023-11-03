# Multiple Instances

**Repo folder** : [src/main/java/B_B40_WaterStateInstance/WaterStateInstance.java](github-repo.md)

<warning>
<p>
<strong>
There is currently a beta version bug we are fixing. Feel free to read this section but it will currently not work.
</strong>
</p>
</warning>

## Introduction
When you work with more complex Test Configurations, you may want to create different instances of the same Class.

When you add a new Instance, it will be added as an orphaned component on the canvas. 

### Instance IDs
A unique Instance ID will be generated as shown below. Vizitest adds a number to the end of the Class name to guarantee uniqueness.

<img src="training-instance-id.png" alt="instance ids" width="900"/>

### Mapping Method to an Instance
For an Instance Component to have any effect on a test, it will usually need to be connected to a Method Component.

As you can see below, the method is associated with WaterStateInstance. The newly **addedWaterStateInstance1** is orphaned.

<img src="training-instance-method-mapping-1..png" alt="instance to method mapping" width="900"/>

You can change the mapping by clicking in the Method Component's pill to reveal a dropdown that lets you change the mapping.

At that point, **WaterStateInstance1** will be connected and **WaterStateInstance** will be orphaned.

### Multiple Methods and Multiple Instances
Normally, if you have multiple Instances, you would connect each one to different Methods. Once that has been done, none of the Instances would be orphaned.


