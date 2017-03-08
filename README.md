# Motor-step
# Arduino motor step test 3d printed

// give it a name:
int salidaPasoZ = 13;
int salidaPasoY = 12;
int salidaPasoX = 11;

int salidaSenZ = 8;
int salidaSenY = 7;
int salidaSenX = 6;
int tiempo = 1;


// the setup routine runs once when you press reset:
void setup() {                
  // initialize the digital pin as an output.
  pinMode(salidaPasoZ, OUTPUT); 
  pinMode(salidaPasoY, OUTPUT); 
  pinMode(salidaPasoX, OUTPUT); 
  
  pinMode(salidaSenZ, OUTPUT); 
  pinMode(salidaSenY, OUTPUT);
  pinMode(salidaSenX, OUTPUT);

}
 
  

// the loop routine runs over and over again forever:
void loop() {
  /*
  a0b0(); // ---------blanco
  delay(tiempo*700);
  */
for(int i=0; i<=60; i++){
    // avance
    tiempo = 200;


   // ------------------------vuekta
   if (i > 30) {
    digitalWrite(salidaPasoZ, HIGH);
    digitalWrite(salidaPasoY, HIGH);
    digitalWrite(salidaPasoX, HIGH);
    digitalWrite(salidaSenZ, LOW);
    digitalWrite(salidaSenY, LOW);
    digitalWrite(salidaSenX, LOW);
    delay(tiempo);
    
    digitalWrite(salidaPasoZ, LOW);
    digitalWrite(salidaPasoY, LOW);
    digitalWrite(salidaPasoX, LOW);
    delay(tiempo);

    
   }
   else {
    digitalWrite(salidaPasoZ, HIGH);
    digitalWrite(salidaPasoY, HIGH);
    digitalWrite(salidaPasoX, HIGH);
    digitalWrite(salidaSenZ, HIGH);
    digitalWrite(salidaSenY, HIGH);
    digitalWrite(salidaSenX, HIGH);
    delay(tiempo);
    
    digitalWrite(salidaPasoZ, LOW);
    digitalWrite(salidaPasoY, LOW);
    digitalWrite(salidaPasoX, LOW);
    delay(tiempo);

   }
    
 }

}

