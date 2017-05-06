# chef-roles

Holding place for all roles for my chef apps.

Create the web and load-balancer roles

```
$ knife role from file roles/web.json
$ knife role from file roles/load-balancer.json
$ knife role list
$ knife role show web
$ knife role show load-balancer
```

Assign the roles to all of your nodes.

```
$ knife node run_list set web1 "role[web]"
$ knife node run_list set web2 "role[web]"
$ knife node run_list set load-balancer "role[load-balancer]"
```

Verify.

```
$ knife node show web1
$ knife node show web2
$ knife node show load-balancer
```
