<div class="top">

# Starting Cassandra
### [◂](command:katapod.loadPage?step6){.steps} Step 7 of 8 [▸](command:katapod.loadPage?step8){.steps}
</div>

Start Cassandra:
```
cassandra
```

Observe the log output while Cassandra is starting. 

Wait for message `Node localhost/127.0.0.1:7000 state jump to NORMAL` and hit <kbd>enter</kbd> or <kbd>return</kbd> in the terminal.

Check the status of Cassandra:
```
nodetool status
```

The status/state column in the output should report `UN`, which stands for Up/Normal.

[continue](command:katapod.loadPage?step8){.orange_bar}
