# Usage
Want to benchmark a tool? Instrument your program to print statistics as
```
DINNER_STAT key value
```
Print as many copies as you want - only the last instance is recorded. Critical arguments are:

- `-f filename` -- input file containing arguments for tool you want to test. The first word on each line is an identifier for that test case, and all the other text gets passed in as an argument to the value of the `-c` flag.
- `-c command` -- combined with the `args` in each line of `filename`, executes
    command *args
on the command line.
- `-o output` -- default log is `output.log`, but you can change that with this flag.
- `-p prefix` -- don't like dinner? replace `DINNER_STAT` with whatever you want.
 
Without configuration, `dinner` only records CPU time. Any output sent to `STDOUT` not prefixed appropriately is ignored.
