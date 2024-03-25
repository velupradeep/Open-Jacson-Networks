## NAME: PRADEEP V
## REG N0:212223240119

# Series Queues with infinite capacity - Open Jackson Network

## Aim :
To find (a) average number of materials in the system (b) average number of materials in the each conveyor of (c) waiting time of each material in the system (d) waiting time of each material in each conveyor, if the arrival  of materials follow Poisson process with the mean interval time 12 seconds, service time of  lathe machine in series follow exponential distribution  with service time  1 second, 1.5 seconds and 1.3 seconds respectively and average service time of robot is 7 seconds.

## Software required :
Visual components and Python

## Theory
![203239736-7b81f599-71a8-4ae7-b63e-5d98acd9ea54](https://github.com/velupradeep/Open-Jacson-Networks/assets/150329341/132d9631-3b93-42b6-98d0-28712665d506)





## Procedure :
![203239789-bc870dce-6727-487b-a0e2-4fc3f5114889](https://github.com/velupradeep/Open-Jacson-Networks/assets/150329341/cafac489-cad8-4031-a668-781de8e6712a)



## Experiment:
![313417375-781b06e3-9d28-4534-8472-3a072c3d03ba](https://github.com/velupradeep/Open-Jacson-Networks/assets/150329341/aadec9f6-879a-4a99-822c-3fa7100ba6fb)
![313417382-1a706359-6d44-43fa-a405-382ff324b0c4](https://github.com/velupradeep/Open-Jacson-Networks/assets/150329341/19651c05-ae33-4c08-9a23-4798ee6e32bd)



## Program
```
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time1=float(input("Enter the mean  inter service time of Lathe Machine 1 (in secs) :  "))
ser_time2=float(input("Enter the mean  inter service time of Lathe Machine 2 (in secs) :  "))
ser_time3=float(input("Enter the mean  inter service time of Lathe Machine 3 (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu1=1/(ser_time1+Robot_time)
mu2=1/(ser_time2+Robot_time)
mu3=1/(ser_time3+Robot_time)
print("-----------------------------------------------------------------------")
print("Series Queues with infinite capacity- Open Jackson Network")
print("-----------------------------------------------------------------------")
if (lam <  mu1) and (lam <  mu2) and (lam <  mu3):
    Ls1=lam/(mu1-lam)
    Ls2=lam/(mu2-lam)
    Ls3=lam/(mu3-lam)
    Ls=Ls1+Ls2+Ls3
    Lq1=Ls1-lam/mu1
    Lq2=Ls2-lam/mu2
    Lq3=Ls3-lam/mu3
    Wq1=Lq1/lam
    Wq2=Lq2/lam
    Wq3=Lq3/lam
    Ws=Ls/(3*lam)
    print("Average number of objects in the system S1 : %0.2f "%Ls1)
    print("Average number of objects in the system S2 : %0.2f "%Ls2)
    print("Average number of objects in the system S3 : %0.2f "%Ls3)
    print("Average number of objects in the overall system    : %0.2f "%Ls)
    print("Average number of objects in the conveyor S1  :  %0.2f "%Lq1)
    print("Average number of objects in the conveyor S2  :  %0.2f "%Lq2)
    print("Average number of objects in the conveyor S3  :  %0.2f "%Lq3)
    print("Average waiting time of an object in the conveyor S1 : %0.2f secs"%Wq1)
    print("Average waiting time of an object in the conveyor S2 : %0.2f secs"%Wq2)
    print("Average waiting time of an object in the conveyor S3 : %0.2f secs"%Wq3)
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("----------------------------------------------------------------------")
```


## Output
![313417363-9e8244ad-040b-47d6-b730-50a9eb12a68a](https://github.com/velupradeep/Open-Jacson-Networks/assets/150329341/a8163081-abbb-4344-b4b0-451206d1c2c1)

## Result
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.
