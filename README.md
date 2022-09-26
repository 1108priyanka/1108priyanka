- 👋 Hi, I’m @1108priyanka
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
1108priyanka/1108priyanka is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
float x,y,z,temp;
void setup()
{
  pinMode(8, INPUT);
  pinMode(5, OUTPUT);
  pinMode(6, OUTPUT);
  pinMode(A5, INPUT); 
  pinMode(A4, INPUT);
Serial.begin(9600);
}
void loop()
{
  x= digitalRead(8);
  y= analogRead(A5);
  z= analogRead(A4);
  Serial.println(x);
  Serial.println(y);
  Serial.println(z);
  temp = (double)z / 1024;       
  temp = temp * 5;                 
  temp = temp - 0.5;               
  temp = temp * 100;               
  if ( (x>0) )
  {
    if ((y<550)&&(temp>30))
    {
      digitalWrite(5, HIGH);
      digitalWrite(6, HIGH);
    }
    else if((y<550)&&(temp<30))
    {
      digitalWrite(5, HIGH);
      digitalWrite(6, LOW);
    }
    else if((y>550)&&(temp>30))
    {
      digitalWrite(5, LOW);
      digitalWrite(6, HIGH);
    }
    else if((y>550)&&(temp<30))
    {
      digitalWrite(5, LOW);
      digitalWrite(6, LOW);
    }
  }
  else
  {
    digitalWrite(5, LOW);
    digitalWrite(6, LOW);
  }
}![spriyanka](https://user-images.githubusercontent.com/114377303/192292785-a9cca755-042f-4ed8-9b3d-d9a20b0fb715.jpeg)

