# Connecting to a codebase

The Test Manager manages a list of Projects. Each project is a codebase you have connected to on your local machine.

<tip>
    <p>
        Please note that the Project list you see in the left sidebar is local to a your PC. If you are working with a Vizitest Project for the first time, you will need to add a new Project as explained here.
    </p>
<p>
        You would typically pull your codebase from a Git repository. If someone else has created a Project in that repository, when you have added your Vizitest Project, you will see all Groups and Test Configurations immediately.
</p>
</tip>


## Creating a Project
To connect, press the '+' icon in the left sidebar next to **Projects**.

<img src="project-add.png" width="400" alt="connect codebase"/>

You will then see the following dialog.

<img src="codebase-connect.png"  alt="connect codebase" width="500"/>


- Choose a Project name
- In the **Path** field, point to the absolute path of the codebase on your local machine. 
- Provide an optional description for the project. This will appear in the Project list when you hover on a Project.
- Choose a color. This is purely a visual aid to help differentiate one Project from another in the left sidebar.

<warning>
    <p>
        The <strong>Path</strong> field must currently point to an IntelliJ root folder.
    </p>
    <p>
        In IntelliJ, you can find the absolute path to your codebase by right-clicking the root folder in the project file tree. You can then select the Absolute path option and paste it into the Vizitest path field.
    </p>
<img src="absolute-path-intellij.png" alt="absolute path" width="600"/>
</warning>

Once you confirm, you will see the new Project in the left sidebar.


## Verifying Vizitest is installed in your codebase
Once you've added a Vizitest Project, you should see a ```.vizitest``` folder in the root of your codebase. This is where all Groups and Test Configurations are stored.

<img src="dot-vizitest-folder.png" alt="vizitest folder" width="400"/>

If you drill into this folder, you will find the Test Manager hierarchy and associated Test Configurations. You can even double click on a ```.tconfig``` file to open it within IntelliJ.
