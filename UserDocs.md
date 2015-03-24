## options ##

| **options** | **type** | **description** | **default value** |
|:------------|:---------|:----------------|:------------------|
| attribute | string | specifies the attribute used to identify checkboxes. For example: if user specifies attribute: "id" and onCheck { 1: { check: '2,3,4' } }, the script will check input with id="2", id="3", id="4" when input with id="1" is checked. | id |
| cascade | boolean | if true, the script acts also if the checkbox's state is changed by the script itself. For example: if user specifies "on check checkbox 1 then check checkbox 2" and "on check checkbox 2 then check checkbox 3" and cascade is set to true, then checking checkbox 1 the script will check checkbox 2 and 3. | false |
| container | string | identifies a group of checkboxes binded to plugin. Usefull when user has more istances of smartcheckbox in the same page. | smartcheckbox`[i]` |
| onCheck | object | is a list that contains each checkbox with associated actions to run when the it is checked. For example: onCheck: { 1: { check: '2,3', uncheck: '4,5', url: 'server.php' } } | null |
| onCheck.i.check | string | list of checkboxes to check separated by coma. |  |
| onCheck.i.uncheck | string | list of checkboxes to uncheck separated by coma. |  |
| onCheck.i.url | string | url to call to retrieve list of actions to perform. The page must return a string like: "{ check: 'x,y,z', uncheck: 'a,b,c'}" |  |
| onUncheck | object |  |  |
| onUncheck.i.check | string |  |  |
| onUncheck.i.uncheck | string |  |  |
| onUncheck.i.url | string |  |  |