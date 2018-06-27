# Naval-Vessel-Maintenance
UCI Data Set

Data Obtained from UCI: http://archive.ics.uci.edu/ml/datasets/condition+based+maintenance+of+naval+propulsion+plants#

Dataset information
The experiments have been carried out by means of a numerical simulator of a naval vessel (Frigate) characterized by a Gas Turbine (GT) propulsion plant. The different blocks forming the complete simulator (Propeller, Hull, GT, Gear Box and Controller) have been developed and fine tuned over the year on several similar real propulsion plants. In view of these observations the available data are in agreement with a possible real vessel.
            
In this release of the simulator it is also possible to take into account the performance decay over time of the GT components such as GT compressor and turbines.

The propulsion system behaviour has been described with this parameters:
    Ship speed (linear function of the lever position lp)
    Compressor degradation coefficient kMc.
    Turbine degradation coefficient kMt
    
so that each possible degradation state can be described by a combination of this triple (lp,kMt,kMc).

The range of decay of compressor and turbine has been sampled with an uniform grid of precision 0.001 so to have a good granularity of representation

In particular for the compressor decay state discretization the kMc coefficient has been investigated in the domain [1; 0.95], and the turbine coefficient in the domain [1; 0.975]

Ship speed has been investigated sampling the range of feasible speed from 3 knots to 27 knots with a granularity of representation equal to tree knots

A series of measures (16 features) which indirectly represents of the state of the system subject to performance decay has been acquired and stored in the dataset over the parameter’s space.

Attribute Information:

A 16-feature vector containing the GT measures at steady state of the physical asset:

    Lever position (lp) [ ]

    Ship speed (v) [knots]

    Gas Turbine (GT) shaft torque (GTT) [kN m]

    GT rate of revolutions (GTn) [rpm]

    Gas Generator rate of revolutions (GGn) [rpm]

    Starboard Propeller Torque (Ts) [kN]

    Port Propeller Torque (Tp) [kN]

    Hight Pressure (HP) Turbine exit temperature (T48) [C]

    GT Compressor inlet air temperature (T1) [C]

    GT Compressor outlet air temperature (T2) [C]

    HP Turbine exit pressure (P48) [bar]

    GT Compressor inlet air pressure (P1) [bar]

    GT Compressor outlet air pressure (P2) [bar]

    GT exhaust gas pressure (Pexh) [bar]

    Turbine Injecton Control (TIC) [%]

    Fuel flow (mf) [kg/s]

A 2 -feature vector containing information about turbine and compressor decay

    GT Compressor decay state coefficient

    GT Turbine decay state coefficient

Goals:
Identify factors that have impact on Compressor decay and relay information to preventative maintence team
Develop and evaluate best model to predict decay state coefficient (logreg,CART,RFC,DNN, etc.)
