# Use YAML Notation in Writing Tasks

**Date: April 24, 2016**

As much as possible write tasks using the YAML notation

Example, from this:

```
- name: Writes to a dummy file
  file: src=/foo/bar dest=/foo/baz state=present
```

to something like this:

```
- name: Writes to a dummy file
  file: 
  	src: /foo/bar 
  	dest: /foo/baz 
  	state: present
```

The previous format is suggested by ansible's official documentation:

- It makes the tests feel like shell scripts, small and concise
- The tasks feel compact and more configuration can be seen in one look
- Many existing roles and playbooks follow this format

But the downsides are:

- You're reading left-to-right
- Worry about converting variable types being converted into strings in some situations
- Git version control differences blot out entire lines as being changed instead of the appropriate attributes.

Using the latter format makes it easier for other developers to keep track of your changes. It's personal preference but moreover it's for team clarity and leveraging version control.

## References:

[1] YAML Practices - http://www.jeffgeerling.com/blog/yaml-best-practices-ansible-playbooks-tasks