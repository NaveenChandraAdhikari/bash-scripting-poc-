## LOOPS
Loops allow us to take a series of commands and keep re-running them until a particular situation is reached
They are useful for automating repetitive tasks

-- we basically learn 3 loops here 
 - for
 - while
 - until

### while do done
  while [<sometask>]
 do 

done

-example
```bash
#!/bin/bash
# Basic while loop
counter=1
while [ $counter -le 10 ]
do
echo $counter
((counter++))
done
echo All done
```


### until loop 
until loop is same as while, the difference it ,it will execute the processs until its true 
until[<some tasks>]
do 
<command>
done 

- example
```bash
#!/bin/bash
# Basic until loop
counter=1
until [ $counter -gt 10 ]
do
echo $counter
((counter++))
done
echo All done
```
### for loop 

for var in <list>
do
<commands>
done


```bash
#!/bin/bash
# Basic for loop
names='Stan Kyle Cartman'
for name in $names
do
echo $name
done
echo All done
```

##### for loop with ranges
```bash
#!/bin/bash
for val in {1..8}
do
echo $val
done
echo All done 
```
```bash
for ((num = 1; num <= 5; num++))
do
echo $num
done
echo All done
```
![image](https://github.com/user-attachments/assets/4d272f30-91ce-4d6e-9f85-a213dc2eb808)


### control loops with break and contune


- break: means leave the loop straight away 
```bash
#!/bin/bash
# Make a backup set of files
for value in $1/*
do
used=$( df $1 | tail -1 | awk '{ print $5 }' | sed 's/%//' )
if [ $used -gt 90 ]
then
echo Low disk space 1>&2
break
fi
cp $value $1/backup/
done
```
- continue : The continue statement tells Bash to stop running through this iteration of the loop and begin the next iteration

```bash
#!/bin/bash
#!/bin/bash
# Make a backup set of files
for value in $1/*
do
if [ ! -r $value ]
then
echo $value not readable 1>&2
continue
fi
cp $value $1/backup/
done
  ```
