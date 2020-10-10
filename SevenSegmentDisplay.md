int a[][7]={
{0,1,1,1,1,1,1}, //'0'code:
{0,0,0,1,0,0,1}, //'1'code:
{1,0,1,1,1,1,0}, //'2'code:
{1,0,1,1,0,1,1}, //'3'code:
{1,1,0,1,0,0,1}, //'4'code:
{1,1,1,0,0,1,1}, //'5'code:
{1,1,1,0,1,1,1}, //'6'code:
{0,0,1,1,0,0,1}, //'7'code:
{1,1,1,1,1,1,1}, //'8'code:
{1,1,1,1,0,0,1}, //'9'code:
{3,4,5,6,7,8,9}  //gfabedc
};
int D1=10,D2=11;
void printChar(int,int,int);
void setup() {
  // put your setup code here, to run once:
pinMode(D1,OUTPUT);
pinMode(D2,OUTPUT);
for(int i=0;i<7;i++)
{
  pinMode(a[10][i],OUTPUT);
}
Serial.begin(9600);
}

void loop() {
  // put your main code here, to run repeatedly:
printChar(96,D1,D2);
}
void printChar(int digit,int Ga,int Gb){
int digit1=digit/10;
int digit2=digit%10;
digitalWrite(Ga,HIGH);
digitalWrite(Gb,HIGH);
for(int i=0;i<7;i++)
{
  digitalWrite(a[10][i],a[digit1][i]);
}
digitalWrite(Ga,LOW);
delay(10);
digitalWrite(Ga,HIGH);
for(int j=0;j<7;j++)
{
  digitalWrite(a[10][j],a[digit2][j]);
}
digitalWrite(Gb,LOW);
delay(10);
digitalWrite(Gb,HIGH);
}
