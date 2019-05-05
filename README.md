Flirc definitions for Arcam FMJ A19
===================================

I've got a setup where Raspberry PI needs to control Arcam FMJ A19. As it doesn't have a digital input I am using
[Flirc](https://flirc.tv/) to replace the original remote.


Usage
-----

All of the dumped commands so far are in [dumps](./dumps) directory. flirc_util is supplied as part of the Flirc SDK - please refer to their website to obtain the binaries.

They can be used as such:

```
>> flirc_util send_ir_raw "$(cat ./dumps/av-down.csv)"
```

Please note the device works by only sending the "DOWN" signal, but the remote itself sends DOWN when the button is first pressed and then UP when it's released.

To do additional dumps
----------------------

```
# to dump all of the sequences to the console
>> flirc_util device_log -i -p
```


Author
------

Andrey Cizov ([acizov@gmail.com](mailto:acizov@gmail.com)) (no copyright)

Dumps have been recorded from the remote control and do not belong to me.
