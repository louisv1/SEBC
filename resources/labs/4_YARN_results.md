I ran the below tests, but more a less the same time always. I suspect that the load is not big enough to create a constrain.
If i send more records I will then probably get more of a constrain and find a sweet spot when changing mappers/reducers. 


8mappers
1reducers
terragen : 1mins, 0sec
terrasort: 2mins, 38sec

terragen : 1min, 2sec
terrasort: 2mins, 48sec


8mappers
2reducers
terragen : 1mins, 1sec
terrasort: 2mins, 7sec

terragen : 55sec
terrasort: 2mins, 14sec


12mappers
4reducers
terragen : 59sec
terrasort: 2mins, 7sec

terragen : 1min, 4sec
terrasort: 2mins, 5sec


4mappers
1reducers
terragen : 53sec
terrasort: 2mins, 39sec

terragen : 55 sec
terrasort: 2mins, 40sec



20mappers
1reducers
terragen : 1mins, 5sec
terrasort: 2mins, 40sec

terragen : 1mins, 3sec
terrasort: 2mins, 42sec

