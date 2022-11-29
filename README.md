# Homework: golfers

The [Social Golfer Problem](https://en.wikipedia.org/wiki/Social_golfer_problem), see also problem description on [CSPLib](https://www.csplib.org/Problems/prob010/).

There are $n=g\times s$ golfers who play golf once per week. Each week they play in $g$ groups of $s$ golfers per group. Create a schedule for $w$ weeks such that __no golfer plays in the same group as any other golfer on more than one occasion__, i.e., maximum socialization. If it is possible, output `yes` and some reasonable representation of the schedule.


An instance is given by the triple of parameters $(g, s, w)$. Running

```
picat golfers.pi 3 2 5
```
should output `yes` and a valid schedule in some reasonable representation, for example:
```
yes
[1,1,1,1,1]
[1,2,2,2,2]
[2,1,2,3,3]
[2,3,3,1,2]
[3,2,3,3,1]
[3,3,1,2,3]
```
where each row represents a schedule for one golfer (there are 6 golfers), the numbers are the groups. The output of 
```
picat golfers.pi 2 2 4
```
should include `failed` (it can be in stderr as Picat normally does).

(This is a hard problem, so don't be surprised if your model won't be able to solve even relatively small instances. The instanc e `8 4 10` was a somewhat well-known open problem, solved only in 1996.)