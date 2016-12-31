Icinga / Nagios Check Script for logged in users
====

Monitor the amount of logged in users. The script uses "w" to determine the open sessions.

Sample usage:

```
object Service "logged-in-users" {
	import "generic-service"

	retry_interval = 5s
	max_check_attempts = 3

	check_command = "logged-in-users"
	host_name = "yourhost"
	command_endpoint = "yourhost"
}
```
Be sure to add a notification to this service! Otherwise it's a bit useless.
