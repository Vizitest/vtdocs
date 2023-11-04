# More on Exceptions

This unit is informational only.

This unit just draws your attention to how exceptions are managed in Vizitest.

If your code throws exceptions you can handle the general **Exception** as well as custom exceptions.

In the Method component's Output column, you have the **Exceptions** section. For each exception you have added to the list you can change the expected exception type using the dropdown.

<warning>
<p>
<strong>
We are currently improving this so the dropdown exception list is sorted and searchable.
</strong>
</p>
</warning>

<img src="custom-exceptions.png" alt="custom assertions" width="900"/>

If you code throws custom exceptions, you can still use the default **Exception**, which catches all exceptions including custom exceptions.
