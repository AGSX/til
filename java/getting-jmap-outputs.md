# Getting JMap Outputs

**Date: April 14, 2016**

To get the profile of objects that are being generated or used during a JVM. This gives greater control on what objects are being spawned. Here's the command to pipe the output to a file.

```
$ (sudo -u kafka /usr/jdk64/jdk1.7.0_67/bin/jmap -histo -F <pid>) 2>&1 | tee jmap-output.txt
```

You'll get a list of the Java object and the amount of instances and total bytes for each object in the java process.

### Troubleshooting

**Can't attach to a process**

Make sure, just like the "Reading JStat" TIL article, to run the `jmap` command you must ensure 3 things:

- Use the same user that ran the process.
- Make sure you use the same java binaries used to launch the same java process. Find out which `java` the process is using, and use the `jmap` for that binary. Example: `/usr/jdk64/jdk1.7/bin/java` was used for launching the java process, then you should use `/usr/jdk64/jdk1.7/bin/jmap`.
- If it still can't attach, run this first: `echo 0 | sudo tee /proc/sys/kernel/yama/ptrace_scope`. Note: works only on Ubuntu. This enables ptrace attachments over ssh. See https://www.kernel.org/doc/Documentation/security/Yama.txt for more details on this.

