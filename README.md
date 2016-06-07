# Problema_4
%Jennifer Lizeth Andrés Jorge
%Ángel Gabriel Elías Díaz

%Tetraedro
%Devuelve el promedio del volumen de los 200 tetraedros.
x=0;%inicializando el valor que será la suma de los volúmenes de los tetraedros formados por puntos aleatorios que están dentro del tetraedro dado
for k=1:200%se enocontrarán los volúmenes para veinte tetraedros
  m=[zeros(4,3) [1;1;1;1]];%inicializando la matriz que será modificada con las coordenadas de los puntos que forman el tetraedro
  for i=1:4
	m(i,1)=rand; %coordenada en x
	m(i,2)=rand*(1-(m(i,1)));%coordenada en y
	m(i,3)=rand*(1-(m(i,1))-(m(i,2)));% coordenada en z
  end
  x=x+abs(det(m)/6);%sumamos todos los volúmenes
end
x/200%encontramos la media de los volúmenes
