SUBJECT : WAD
Sample Program
1  The EventEmitter Object

In the example below we have created a function that will be executed when a "scream" event is fired.
To fire an event, use the emit() method.
var events = require('events');
var eventEmitter = new events.EventEmitter();

//Create an event handler:
var myEventHandler = function () {
  console.log('I hear a scream!');
}

//Assign the event handler to an event:
eventEmitter.on('scream', myEventHandler);

//Fire the 'scream' event:
eventEmitter.emit('scream');

2. jQuery UI Example
3. 
<!DOCTYPE html>  
<head>  
  <link href="http://code.jquery.com/ui/1.10.4/themes/ui-lightness/jquery-ui.css" rel="stylesheet">  
  <script src="http://code.jquery.com/jquery-1.10.2.js"></script>  
<script src="http://code.jquery.com/ui/1.10.4/jquery-ui.js"></script>  
  <style>  
  #draggable { width: 100px; height: 100px; padding: 0.5em; background:#7fffd4;}  
  </style>  
 <script>  
  $(function() {  
    $( "#draggable" ).draggable();  
  });  
  </script>  
</head>  
<body>  
     <div id="draggable" class="ui-widget-content">  
      <p>I am draggable!</p>  
     </div>  
</body>  
</html>  

Output :  I am draggable!

3 jQuery Example

<!DOCTYPE html>  
<html>  
<head>  
 <title>First jQuery Example</title>  
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js">  
 </script>  
 <script type="text/javascript" language="javascript">  
 $(document).ready(function() {  
 $("p").css("background-color", "pink");  
 });  
 </script>  
 </head>  
<body>  
<p>This is first paragraph.</p>  
<p>This is second paragraph.</p>  
<p>This is third paragraph.</p>  
</body>  
</html>  

Output:
This is first paragraph.
75Hello Java Program for Beginners
This is second paragraph.
This is third paragraph.

4  Example to see the use of Tag selector. This would select all the elements with a tag name and the background color is set to "pink".
<!DOCTYPE html>  
<html>  
<head>  
 <title>First jQuery Example</title>  
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js">  
 </script>  
 <script type="text/javascript" language="javascript">  
 $(document).ready(function() {  
 $("p").css("background-color", "pink");  
 });  
 </script>  
 </head>  
<body>  
<p>This is first paragraph.</p>  
<p>This is second paragraph.</p>  
<p>This is third paragraph.</p>  
</body>  
</html>  

Output:
This is first paragraph.
This is second paragraph.
This is third paragraph.
5  Example to see the jQuery hide effect.

<!DOCTYPE html>  
<html>  
<head>  
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>  
<script>  
$(document).ready(function(){  
    $("#hide").click(function(){  
        $("p").hide();  
    });  
});  
</script>  
</head>  
<body>  
<p>  
<b>This is a little poem: </b><br/>  
Twinkle, twinkle, little star<br/>  
How I wonder what you are<br/>  
Up above the world so high<br/>  
Like a diamond in the sky<br/>  
Twinkle, twinkle little star<br/>  
How I wonder what you are  
</p>  
<button id="hide">Hide</button>  
</body>  
</html>  
6. Simple CSS example
<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: lightblue;
}

h1 {
  color: white;
  text-align: center;
}

p {
  font-family: verdana;
  font-size: 20px;
}
</style>
</head>
<body>

<h1>My First CSS Example</h1>
<p>This is a paragraph.</p>

</body>
</html>

7.  Bootstrap
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
</head>
<body>

<div class="container">
  <h1>My First Bootstrap Page</h1>
  <p>This is some text.</p>
</div>

</body>
</html>
 8  write a simple example using AngularJS library. Let us create an HTML file
<!doctype html>
<html>
<head>
<scriptsrc="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.2/angular.min.js"></script>
</head>
<bodyng-app="myapp">
<divng-controller="HelloController">
<h2>Welcome {{helloTo.title}} to the world of
Tutorialspoint!</h2> </div>
<script>
angular.module("myapp",[])
.controller("HelloController",function($scope){
$scope.helloTo={};
$scope.helloTo.title="AngularJS";
});
</script>
</body>
</html>
9   Write html code for form (representative code is mentioned here, modify for multiple inputs)
<h1>Simple Form</h1>
<form#simpleForm = "ngForm"(ngSubmit) = "getValues(simpleForm.value)">
  <inputtype ="text"ngModelname = "user"placeholder = "Enter Name">
  <br><br>
  <inputtype ="text"ngModelname = "age"placeholder = "Enter age">
  <br><br>
  <inputtype ="text"ngModelname = "city"placeholder = "Enter city">
  <br><br>
  <button>Get user value</button>
</form>

10. Sample code :
Ajax communication.html
<html>
<body>
<div id="xyz">
            Hello Friends <br>
            Welcome to Pune!!!!!<br>
<button type="button" onclick="load()">
            Submit
</button>
</div>
<script>
            function load(){
                var req=new XMLHttpRequest()
                req.onreadystatechange=function() {
                    if(this.readyState == 4 && this.status == 200){
                        document.getElementById("xyz").innerHTML=this.responseText
                    }
                }
                req.open('GET','data.txt',true)
                req.send()
            }
</script>

</body>
</html>


##Date Program##
date.component.ts


import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-date',
  templateUrl: './date.component.html',
  styleUrls: ['./date.component.css']
})
export class DateComponent implements OnInit {

message : string = new Date().toDateString();
/*
dateMessage :string;

  constructor() {
    let currentDate = new Date();
    this.dateMessage = currentDate.toDateString() + ' ' + currentDate.toLocaleTimeString();
   }
*/
dateMessage : string = "";
constructor() {
 setInterval(() => {
   let currentDate = new Date();
   this.dateMessage = currentDate.toDateString() + ' ' + currentDate.toLocaleTimeString();
 },1000);
  
 }
  ngOnInit(): void {
  }

}


#####CLIENT>JAVA###
import java.io.*;
import java.net.Socket;
import java.util.Scanner;

public class client{
      private static DataOutputStream dataOutputStream =null;
      private static DataInputStream dataInputStream =null;
      private static Scanner scanner =new Scanner(System.in);
      
      
      public static void main(String[] args){
        try(Socket socket =new Socket("Localhost",5000)){
        
      dataInputStream= new DataInputStream(socket.getInputStream());

dataOutputStream = new DataOutputStream(socket.getOutputStream());

while (true) {

System.out.print("input> " );

String message =scanner.nextLine();

dataOutputStream.writeUTF(message);
 if(message.equalsIgnoreCase("exit()"))
  break;
 }

}catch (Exception e){

System.out.println(e.toString());
      
      }
      
}
}

######SERVER>JAVA#####
import java.io.*;

import java.net.ServerSocket;

import java.net.Socket;

public class server {

private static DataOutputStream dataOutputStream = null; 
private static DataInputStream dataInputStream = null;

public static void main(String[] args) {
 try(ServerSocket serverSocket = new ServerSocket(5000)) {

System.out.println("Listening to port:5000");
 Socket clientSocket= serverSocket.accept();

System.out.println(clientSocket+" connected\n");

dataInputStream=new DataInputStream(clientSocket.getInputStream()); 
dataOutputStream = new DataOutputStream (clientSocket.getOutputStream());

String message; 
while (true) {

message = dataInputStream.readUTF(); 
System.out.println(message); 
if(message.equalsIgnoreCase("exit()"))

break;

}
clientSocket.close();

}catch(Exception e) {
 System.out.println(e.toString());

}
}
}

##############RR####################

// Java program for implementation of RR scheduling
 
public class RoundRobin
{
    // Method to find the waiting time for all
    // processes
    static void findWaitingTime(int processes[], int n,
                 int bt[], int wt[], int quantum)
    {
        // Make a copy of burst times bt[] to store remaining
        // burst times.
        int rem_bt[] = new int[n];
        for (int i = 0 ; i < n ; i++)
            rem_bt[i] =  bt[i];
      
        int t = 0; // Current time
      
        // Keep traversing processes in round robin manner
        // until all of them are not done.
        while(true)
        {
            boolean done = true;
      
            // Traverse all processes one by one repeatedly
            for (int i = 0 ; i < n; i++)
            {
                // If burst time of a process is greater than 0
                // then only need to process further
                if (rem_bt[i] > 0)
                {
                    done = false; // There is a pending process
      
                    if (rem_bt[i] > quantum)
                    {
                        // Increase the value of t i.e. shows
                        // how much time a process has been processed
                        t += quantum;
      
                        // Decrease the burst_time of current process
                        // by quantum
                        rem_bt[i] -= quantum;
                    }
      
                    // If burst time is smaller than or equal to
                    // quantum. Last cycle for this process
                    else
                    {
                        // Increase the value of t i.e. shows
                        // how much time a process has been processed
                        t = t + rem_bt[i];
      
                        // Waiting time is current time minus time
                        // used by this process
                        wt[i] = t - bt[i];
      
                        // As the process gets fully executed
                        // make its remaining burst time = 0
                        rem_bt[i] = 0;
                    }
                }
            }
      
            // If all processes are done
            if (done == true)
              break;
        }
    }
      
    // Method to calculate turn around time
    static void findTurnAroundTime(int processes[], int n,
                            int bt[], int wt[], int tat[])
    {
        // calculating turnaround time by adding
        // bt[i] + wt[i]
        for (int i = 0; i < n ; i++)
            tat[i] = bt[i] + wt[i];
    }
      
    // Method to calculate average time
    static void findavgTime(int processes[], int n, int bt[],
                                         int quantum)
    {
        int wt[] = new int[n], tat[] = new int[n];
        int total_wt = 0, total_tat = 0;
      
        // Function to find waiting time of all processes
        findWaitingTime(processes, n, bt, wt, quantum);
      
        // Function to find turn around time for all processes
        findTurnAroundTime(processes, n, bt, wt, tat);
      
        // Display processes along with all details
        System.out.println("PN " + " B " +
                      " WT " + " TAT");
      
        // Calculate total waiting time and total turn
        // around time
        for (int i=0; i<n; i++)
        {
            total_wt = total_wt + wt[i];
            total_tat = total_tat + tat[i];
            System.out.println(" " + (i+1) + "\t\t" + bt[i] +"\t " +
                              wt[i] +"\t\t " + tat[i]);
        }
      
        System.out.println("Average waiting time = " +
                          (float)total_wt / (float)n);
        System.out.println("Average turn around time = " +
                           (float)total_tat / (float)n);
    }
     
    // Driver Method
    public static void main(String[] args)
    {
        // process id's
        int processes[] = { 1, 2, 3};
        int n = processes.length;
      
        // Burst time of all processes
        int burst_time[] = {10, 5, 8};
      
        // Time quantum
        int quantum = 2;
        findavgTime(processes, n, burst_time, quantum);
    }
}


##################FIREBASE ASSIGNMENT#####################
************INDEX********************
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="    viewport" content="width=device-width, initial-scale=1.0">

<script src="https://www.gstatic.com/firebasejs/8.2.7/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/8.2.7/firebase-auth.js"></script>
<script src="form.js"></script>
    <title>Login System</title>
</head>
<body>
    <div class="formContainer">
    <h1>Enter Credentials Here:</h1>
    <input type="email" placeholder="email here" id="email"><br>
    <input type="password" placeholder="password here" id="password"><br>
    <button onclick="signUp()" id="signUp">SignUp</button>
    <button onclick="signIn()" id="signIp">SignIn</button>
    <button onclick="signOut()" id="signOut">SignOut</button>
</div>


    
</body>
</html>

**************************form.js******************
var firebaseConfig = {
    apiKey: "AIzaSyAVH4Wps4AhjUubPWX2vLfHx1pHDaGLrb0",
    authDomain: "project1-3da6c.firebaseapp.com",
    projectId: "project1-3da6c",
    storageBucket: "project1-3da6c.appspot.com",
    messagingSenderId: "810238021634",
    appId: "1:810238021634:web:b1c2f38715403b31ef571b",
    measurementId: "G-8147LMM5P2"
  };
  // Initialize Firebase
  firebase.initializeApp(firebaseConfig);

  const auth =  firebase.auth();

  //signup function
  function signUp(){
    var email = document.getElementById("email");
    var password = document.getElementById("password");

    const promise = auth.createUserWithEmailAndPassword(email.value,password.value);
    //
    promise.catch(e=>alert(e.message));
    alert("SignUp Successfully");
  }

  //signIN function
  function  signIn(){
    var email = document.getElementById("email");
    var password  = document.getElementById("password");
    const promise = auth.signInWithEmailAndPassword(email.value,password.value);
    promise.catch(e=>alert(e.message));
    
  }


  //signOut

  function signOut(){
    auth.signOut();
    alert("SignOut Successfully from System");
  }

  //active user to homepage
  firebase.auth().onAuthStateChanged((user)=>{
    if(user){
      var email = user.email;
      alert("Active user "+email);

    }else{
      alert("No Active user Found")
    }
  })
