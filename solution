/*********************************************
 * OPL 12.6.0.0 Model
 * Cider
 *********************************************/

//Data declarations.
//Make sure you use c[i] to access the i-th data 
//and do not remove/change the following line
float c[1..4] = [-1500,4, 8, 10];

//Decision variables.
dvar float x1;
dvar float x2;
dvar float x3;
dvar float x4;

//Objective function.
maximize c[1]*(x1+x2)+c[2]*(500*x1-x3)+c[3]*(250*x2-x4+0.6*x3)+c[4]*(0.4*x4);

//Constraints
subject to {
    0.4*x4<=500;
    0.4*x4>=0;
    
    x1+x2>=0;

    500*x1-x3<=5000;
    500*x1-x3>=0;
    
    250*x2 - x4 + 0.6*x3 <=2000;
    250*x2 - x4 + 0.6*x3 >=0;
    
    x1>=0;
    x2>=0;
    x3>=0;
    x4>=0;
    
}

// Display
execute {
  writeln("Post treatment: ");
  writeln("The objectif's value is  "+cplex.getObjValue());
} 