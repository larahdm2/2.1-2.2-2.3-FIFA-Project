
![image](https://github.com/larahdm2/FIFA-Project/assets/138598135/7685c657-263a-4f08-8ebf-d510b0fc25f0)


# LAB | FIFA Game

<details>
  <summary>
   <h2>Objective</h2>
  </summary>

This is a team project where we are required to generate a model that predicts the overal rating (OVR) of a FIFA game.

  <br>
  <hr> 

</details>

<details>
  <summary>
   <h2>Description of the data</h2>
  </summary>

Based on our research and knowledge, the OVR is the summation of the player attributes and the international reputation: OVR = ATT + IR .
Although the process of calculating the attributes is more complex, the list of attributes can be resumed in yelow in the picture:
 
  <br>
  
  ![image](https://github.com/larahdm2/FIFA-Project/assets/138598135/d448aebf-551e-4aa7-b9d6-b4faa853b096)
 
  <br>

The percentage of attributes that are considered to calculate the OVR dependes on the player´s position on the pitch (not all attributes are considered important for the position).

Our extract of data includes these attributes. Taking a quick look, we can notice some columns are the result of mathematical operations of others. For example, we think that the first number of those columns that follows the pattern "number+number" can be calculated from other columns.

<br>
<hr> 

</details>

<details>
  <summary>
   <h2>Decisions</h2>
  </summary>

1. The first decision we took was to extract the right number of the columns that contain "number+number", and discard the left number. We supposed (after a few operations) that the left number is the result of mathematical opperations from other columns we are keeping, and that the model will be able to learn.

2. Then, although we got some columns that were the sumation of others, and therefore less columns to play with; we decided to keep all the attributes because we believe they are valuable to learn the result of other columns. So, for example here, we decided to discard Attaking and keep the rest:

   <br>
   
  ![image](https://github.com/larahdm2/FIFA-Project/assets/138598135/06904805-3bbf-48d2-bc3f-1fa405d3741f)


  <br>
  
3. With this information, we launched some draft calculations in python. We checked the correlation between our target and the variables. At first, we decided to discard those variables with little correlation to the model. But we checked how it affected to the model and we got a better result considering all the variables. 

4. Finally, we introduced other variable that is not part of the main formula, but that we always had an intinct it could help the model. 

<br>
<hr> 

</details>
