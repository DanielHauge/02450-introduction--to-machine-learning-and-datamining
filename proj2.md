# Q2
Ir := 1 - (33 + 4)/135;

                                 98 
                           Ir := ---
                                 135

Inot2 := 1 - (33 + 4)/134;

                                   97 
                          Inot2 := ---
                                   134

I2 := 1 - 1*1;
                            I2 := 0

Delta := Ir + (-134/135*Inot2 - 1/135*I2);
                                    1 
                          Delta := ---
                                   135

                           0.0074074
Svar C.

# Q3

Der er 7 attributes der hver har en "styrke/weight" ind på hver hidden unit.
7*10.

output kan tage 4 forskellige diskrette værdier, derfor er der et ouput lag med 4 enheder som hver unit i hidden layer skal forbindes med.
4*10

derfor:

7*10 + 4*10 = 110
Svar C



# Q4
Svaret er D.
Can be easily seen by picking the only choice that enables correctness for Congestion level 4.
Congestion 4 is easly infered to be when b_1 (PCA1) is larger than little below 0. (Big white field)
For Congestion level 4 to be true, choice C has to be true. However, conditions on b_2 for choice C makes no sense.

# Q5

single ANN: 20 / 5
single REG: 8 / 1

- Test 5 times
    - Train 4 times
        - Train 5 times
        - Test 5 times
    - Test 4 times
- Validate 5 times

((20 * 5 + 5 * 5) * 4 + 4 * 5) * 5 + 5 * 5
((8 * 5 + 5 * 1) * 4 + 4 * 1) * 5 + 5

Svar C


# Q6

NULL;
w[1] := <1.2, -2.1, 3.2>;
                             [    1.2     ]
                             [            ]
                     w[1] := [&uminus0;2.1]
                             [            ]
                             [    3.2     ]

w[2] := <1.2, -1.7, 2.9>;
                             [    1.2     ]
                             [            ]
                     w[2] := [&uminus0;1.7]
                             [            ]
                             [    2.9     ]

w[3] := <1.3, -1.1, 2.2>;
                             [    1.3     ]
                             [            ]
                     w[3] := [&uminus0;1.1]
                             [            ]
                             [    2.2     ]

y1 := w[1];
                            [    1.2     ]
                            [            ]
                      y1 := [&uminus0;2.1]
                            [            ]
                            [    3.2     ]

y2 := b1 -> b1*w[2];
   y2 := proc (b1) options operator, arrow, function_assign; 

      b1*w[2] end proc


y3 := b2 -> b2*w[3];
   y3 := proc (b2) options operator, arrow, function_assign; 

      b2*w[3] end proc



y2(-1.4);
                  [&uminus0;1.68000000000000]
                  [                         ]
                  [    2.38000000000000     ]
                  [                         ]
                  [&uminus0;4.06000000000000]


evalHygge := (b1, b2) -> evalf(1/(1 + exp(y1[1]) + exp(y2(b1)[2]) + exp(y3(b2)[3])));

evalHygge(-1.4, 2.6);
                      0.00312470761775071


evalHygge(-0.6, -1.6);
                       0.140392036746439

evalHygge(2.1, 5.0);
                     0.0000167004879415101

evalHygge(0.7, 3.8);
                      0.000233791301408548


SVAR B fordi sanynligheden her er klart stødsrst.


- Explain Q4,Q5,Q6