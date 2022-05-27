# Bug List

> Make a list of the things that don't work as expected. Keep a list of things that you have fixed and try to document how you solved them.

> Current bugs: None.
> 
> Fixed bugs: The algorithm bug!
> This was a bug that would make one of the players win even though they didnt have a three in a row.
> // This for-loop checks all the winning conditions too but this one has a false wining condition in it aswell.
> // function checkEverything() {
> //     for (var i = playingBoard.length - 1; i >= 0; i--) {
> //         // console.log("in the for loop");
> //         checkRow(i);
> //         checkCol(i);
> //         checkDiag(i);
> //         checkOthDiag(i);
> //     }
> // } 
> // This happens when the playingboard looks like this playingBoard = ["X", "O", "X",
>                                                                 //   "O", "X", "O",
>                                                                 //   "", "", ""
>                                                                 //   ];
> // This is the only false winning condition that I can find and I fix it by looping the with loops with diffrent amount of steps.
> // This for-loop checks all the winning conditions and does not produce any false winning conditions.
> // function checkEverything() {
> //     for (var i = 0; i <= playingBoard.length; i+=3) {
> //         checkRow(i);
> //         for (var j = 0; j <= playingBoard.length; j++) {
> //             checkCol(j);
> //             for (var k = 0; k <= playingBoard.length; k+=4) {
> //                 checkDiag(k);
> //                 for (var l = 2; l <= playingBoard.length; l +=2) {
> //                 checkOthDiag(l);    
> //                 }   
> //             }
> //         }
> //     }
> // }
> // Making this work for every grid size then it should be only adding the gridsize and change the numbers around.
> // var grid = 3;
> //   function checkEverything() {
> //     for (var i = 0; i <= playingBoard.length; i + grid) {
> //         checkRow(i);
> //         for (var j = 0; j <= playingBoard.length; j++) {
> //             checkCol(j);
> //             for (var k = 0; k <= playingBoard.length; k + grid + 1) {
> //                 checkDiag(k);
> //                 for (var l = 2; l <= playingBoard.length; l + grid + 2) {
> //                 checkOthDiag(l);    
> //                 }   
> //             }
> //         
> //     }
> // }
> // By not having the loop in side of a loop then I can use var i in every loop. This also 
> // prevents the last winning condition from looping a bunch of times when the condition
> // is met. This is the loop that I will be using in my tic tac toe program. Here I also added
> // the function for O player.
> // This is the grid size. 
> // var grid = 3; 
> //   function checkEverything() {
> //     for (var i = 0; i <= playingBoard.length; i += grid) {
> //         checkXRow(i);
> //         checkORow(i);
> //     }
> //     for (var i = 0; i <= playingBoard.length; i ++) {
> //         checkXCol(i);
> //         checkOCol(i);
> //     }
> //     for (var i = 0; i <= playingBoard.length; i += grid +1) {
> //         checkXDiag(i);
> //         checkODiag(i);
> //     }
> //     for (var i = 2; i <= playingBoard.length; i += grid -1) {
> //         checkOthXDiag(i);
> //         checkOthODiag(i);    
> //     }   
> // } 
> 
> This was the biggest bug I had and the only one that I have documented outside the index.html file. 
