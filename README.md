--Codigo creado para codificar el resultado de la suma de 4 a 8 bits  

LIBRARY IEEE;
USE ieee.std_logic_1164.all;
---------------------------------------------------
ENTITY bcd_1 IS
 PORT( resre : IN  STD_LOGIC_VECTOR(3 DOWNTO 0);--Resultado de la resta de 4 bits
       Cout1 : IN  STD_LOGIC;--Carry final de la resta de 4 bits
		 resret: OUT STD_LOGIC_VECTOR(7 DOWNTO 0));--Resultado de la resta codificada de 4 a 8 bits
END ENTITY	bcd_1;
---------------------------------------------------
ARCHITECTURE bin_to_bcd OF bcd_1 IS 
BEGIN 

		resret(0) <= resre(0);--A los primeros 4 bits se les asigna el valor de cada posicion del resre
		resret(1) <= resre(1);
		resret(2) <= resre(2);
		resret(3) <= resre(3);
		resret(4) <= Cout1;--Se coloca tambien el Cout1 o el carry final en las otras 4 posiciones de los bits
		resret(5) <= Cout1;
		resret(6) <= Cout1;
		resret(7) <= Cout1;
END ARCHITECTURE bin_to_bcd; 
