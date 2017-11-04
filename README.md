# Telegram_MathBattle_Solver
A Simple JS hack to solve telegram math battle problems.

# Usage:
- Run telegram on any web browser.
- In any group chat, run Math Battle game using @gamebot Math Battle.
- Inject JQuery into the web page.
- Define the following functions in the developer console:
```javascript
function mathBattleSolver(){
	xxx= $("#task_x").text();
	yyy= $("#task_y").text();
	opp= $("#task_op").text();
	res= $("#task_res").text();
	if(opp=="+" && (xxx+yyy) == res){
		$("#button_correct").click();
	}
	else if (opp=="–" && (xxx-yyy) == res){
		console.log("Correct");
		$("#button_correct").click();
	}
	else if (opp=="×" && (xxx*yyy) == res){
		$("#button_correct").click();
		console.log("Correct");
	}
	else if (opp=="/" && (xxx/yyy) == res){
		$("#button_correct").click();
		console.log("Correct");
	}
	else{
		console.log("Wrong");
		$("#button_wrong").click();
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
