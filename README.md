# ga_midtest
Midtest about Genetic Algorithm Case

Nadhifa Sofia 
19/448721/PPA/05804

A wood craftsman wants to make a tube-shaped decoration without a lid. The tube is expected to hold a liquid of not less than 200. Help the craftsman to design the tube with minimal materials using genetic algorithms.
Answer : 
1. Problem Formulation
The number of materials required is  equal to the surface of the lidless tube. So, the formula of surface area of a tube without the lid is :
A(r,t) = 2 * phi * r * t  +  phi * r * r
where the area formula is based on the combination of area formula for tube + area formula for circle;
phi = 22/7 or 3.14
r = radius
t = height

Since the tube is expected to hold a liquid with less than 200, so the math formula for lidless tube volume :
V(r,t) = phi * r * r * t >= 200
To sum up, the problem formulation should minimize A(r,t) with restraint of;
r > 0
t > 0
V(r,t) >= 200


2. Chromosomes representation 
The chromosomes that will be generated are based on r and t that we defined in advance. Those 2 are positive real numbers as phi is involved. Hence, the individual will be composed of 2 real positive numbers genes. 
C1 = (r, t)


3. Fitness Function
The penalty method will be used so that the chromosomes can still survive in the population even if it violates the constraints. However, violating chromosomes' fitness values will be penalized for having a much lower fitness value.
F (A, V) = fitness function
F (A, V) = 1/A,            if V >=200
F (A, V) = 10^-8 V,    if V < 200
A smaller surface area will make the fitness value bigger, but violating the volume limit will be excessive so that it actually decreases the fitness value.


4. Generate Initial Population
INPUT: number of chromosomes, radius of upper bound, height of upper limit
OUTPUT: chromosome population

Chromosome 0 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Chromosome 1 :
-radius :  9.653101188131737
-height :  9.48345030463475
-surface area :  867.9333735657469
-volume :  2776.1949686511493
-fitness :  0.0011521621710335681
Chromosome 2 :
-radius :  10.145530389022685
-height :  1.9103470270497018
-surface area :  445.1471998133061
-volume :  617.7484318889058
-fitness :  0.0022464479174965
Chromosome 3 :
-radius :  8.48134257586777
-height :  13.320122890537473
-surface area :  935.8120359851042
-volume :  3010.1442998142606
-fitness :  0.001068590658750533
Chromosome 4 :
-radius :  8.964934291140148
-height :  7.012185704955071
-surface area :  647.4747532341789
-volume :  1770.5064091659813
-fitness :  0.001544461764732809
Chromosome 5 :
-radius :  11.038187989156427
-height :  8.42403135658231
-surface area :  967.0251881125517
-volume :  3224.5225600897356
-fitness :  0.00103409922749976


5. Parental Selection Method by using Baker’s SUS
6. Matting Pool Size : 10
INPUT : population, number of parents to select (default 10)
OUTPUT : selected parents

Selected Parent 0 :
-radius :  9.653101188131737
-height :  9.48345030463475
-surface area :  867.9333735657469
-volume :  2776.1949686511493
-fitness :  0.0011521621710335681
Selected Parent 1 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent 2 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent 3 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent 4 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent 5 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent 6 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent 7 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent 8 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent 9 :
-radius :  4.182391545333953
-height :  8.256814309525463
-surface area :  271.93267791753607
-volume :  453.74491009514145
-fitness :  0.0036773807681298653


5. Do Crossover with Pc = 0.8
selectParents
INPUT : parents , PC
OUTPUT : selected parents based on PC
Crossover - Whole arithmetic crossover will be employed
INPUT : 2 Chromosomes for parents, alpha
OUTPUT : 2 Chromosomes for offspring

Selected Parent from Crossover 0 :
-radius :  9.653101188131737
-height :  9.48345030463475
-surface area :  867.9333735657469
-volume :  2776.1949686511493
-fitness :  0.0011521621710335681
Selected Parent from Crossover 1 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent from Crossover 2 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent from Crossover 3 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Selected Parent from Crossover 4 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528

The offspring after crossover, with Offspring size = selected parent size * (selected parent size - 1)
Offspring from Crossover 0 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 1 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 2 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 3 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 4 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 5 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 6 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 7 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 8 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 9 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 10 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 11 :
-radius :  9.428666853760499
-height :  8.90549132358911
-surface area :  806.8664892464574
-volume :  2487.1864293069957
-fitness :  0.0012393624141385676
Offspring from Crossover 12 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Offspring from Crossover 13 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Offspring from Crossover 14 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Offspring from Crossover 15 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Offspring from Crossover 16 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Offspring from Crossover 17 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Offspring from Crossover 18 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528
Offspring from Crossover 19 :
-radius :  9.20423251938926
-height :  8.32753234254347
-surface area :  747.7461259891968
-volume :  2216.365409340458
-fitness :  0.0013373522981173528


8. Do mutation with Pm = 0.1
Uniform mutation
INPUT : chromosome
OUTPUT : mutated chromosome

--Offspring 16 is mutated
Before mutation r= 9.20423251938926 , t =  8.32753234254347
After mutation r= 9.20423251938926 , t =  0.17976281726188842


9. Do survivor selection / update generation : Generational Model
Combine initial population with offspring, then filter the best 
𝑝𝑜𝑝𝑢𝑙𝑎𝑡𝑖𝑜𝑛𝑆𝑖𝑧𝑒
 chromosomes.
INPUT : population, populationSize
OUTPUT : a population of best 
𝑝𝑜𝑝𝑢𝑙𝑎𝑡𝑖𝑜𝑛𝑆𝑖𝑧𝑒
 chromosomes

Next generation's chromosomes
Chromosome 0
-radius :  9.20423251938926
-height :  0.17976281726188842
-surface area :  276.5451455598025
-volume :  47.843715722291655
-fitness :  0.4784371572229166
Chromosome 1
-radius :  2.9996286674094246
-height :  8.32753234254347
-surface area :  185.2181920458737
-volume :  235.39714529301855
-fitness :  0.005399037691461356
Chromosome 2
-radius :  5.135344339138556
-height :  8.32753234254347
-surface area :  351.5481563317164
-volume :  689.9304928921284
-fitness :  0.0028445605018517367
Chromosome 3
-radius :  10.145530389022685
-height :  1.9103470270497018
-surface area :  445.1471998133061
-volume :  617.7484318889058
-fitness :  0.0022464479174965
Chromosome 4
-radius :  9.20423251938926
-height :  6.10236262853447
-surface area :  619.0603368772863
-volume :  1624.138446876901
-fitness :  0.0016153514293037736
Chromosome 5
-radius :  8.964934291140148
-height :  7.012185704955071
-surface area :  647.4747532341789
-volume :  1770.5064091659813
-fitness :  0.001544461764732809


10. Number of Generations
Chromosome with best fitness value after 1000 iterations:
-radius :  2.5449274178771297
-height :  9.825934157203386
-surface area :  177.4661626924485
-volume :  199.92841528313048
-fitness :  1.9992841528313048
