# Telegram_MathBattle_Solver
A Simple JS hack to solve telegram math battle problems.

# Usage:
- Run telegram on any web browser.
- In any group chat, run Math Battle game using @gamebot Math Battle.
- Define the following functions in the developer console:
```javascript
function mathBattleSolver(){
	xxx= document.getElementById("task_x").innerHTML;
	yyy= document.getElementById("task_y").innerHTML;
	opp= document.getElementById("task_op").innerHTML;
	res= document.getElementById("task_res").innerHTML;
	if(opp=="+" && (xxx+yyy) == res){
		document.getElementById("button_correct").click();
	}
	else if (opp=="–" && (xxx-yyy) == res){
		console.log("Correct");
		document.getElementById("button_correct").click();
	}
	else if (opp=="×" && (xxx*yyy) == res){
		document.getElementById("button_correct").click();
		console.log("Correct");
	}
	else if (opp=="/" && (xxx/yyy) == res){
		document.getElementById("button_correct").click();
		console.log("Correct");
	}
	else{
		console.log("Wrong");
		document.getElementById("button_wrong").click();
	}
}

function mathBattleCaller(numOfTimes){
	while(numOfTimes!=0){
		numOfTimes=numOfTimes-1;
		mathBattleSolver();
	}
}
```
- Call mathBattleCaller function with the number of times you want to score a correct answer, ex: 
```
mathBattleCaller(53); // To get a score of 53.
```

# Changes
- 11/4/2017 : No need to inject JQuery in order to run the functions.
- 11/11/2016 : Initial release (not on github)
