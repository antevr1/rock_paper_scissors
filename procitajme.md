

    function getComputerChoice(){
        let randomNumber = Math.random();
        
        if (randomNumber <= (1/3)){
            return 'rock';
        }
        else if (randomNumber > (1/3) && randomNumber <= (2/3)){
            return 'paper';
        }
        else{
            return 'scissors';
        } 
    };
    let computerChoice = getComputerChoice();


 let playerChoice = window.prompt("Choose rock, paper or scissors.");
    let smallPlayerChoice = playerChoice.toLowerCase();

    if(smallPlayerChoice != 'rock' && playerChoice != 'scissors' && playerChoice != 'paper'){
        console.log('Wrong choice!');
    }

    function chooseWinner(smallPlayerChoice,computerChoice){
        if (smallPlayerChoice == 'rock' && computerChoice == 'paper'){
            console.log('YOU LOSE - the computer chose paper.');
        }
        else if (smallPlayerChoice == 'rock' && computerChoice == 'scissors'){
            console.log('YOU WIN - the computer chose scissors.');
        }
        else if (smallPlayerChoice == 'rock' && computerChoice == 'rock'){
            console.log('DRAW - the computer chose rock.');
        }
    }
    chooseWinner(smallPlayerChoice,computerChoice);