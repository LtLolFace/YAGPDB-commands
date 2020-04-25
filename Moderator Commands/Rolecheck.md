{{$x := (userArg .User.ID).Mention}}
{{if targetHasRoleID $x RoleNumID}}
/* Find RoleNumID by using command listroles. */
Rolecheck passed!
/* Insert custom text here. */
{{exec "role" "RoleName"}}
/* This is the name of the role that you want to assign. It is case sensitive. */
{{else}}
Rolecheck failed!
/* Insert custom text here.*/
{{end}}
 
{{deleteResponse 5}}
{{deleteTrigger 5}}
/* This is the amount of time the user command and response will stay up until being deleted in seconds. */
/* You must allow the YAGPDB to delete and manage other users messages if you want it to clean up after itself. */