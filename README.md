using Promocionado.Class;

Promo promo = new Promo();

promo.Promocionado();

Console.Read();


namespace OperacionDosNumeros.Class
{
    public class Numeros
    {
        public void OperacionDosNumeros()
        {
            int Num1 = 0;
            int Num2 = 0;

            try
            {
                Console.WriteLine("Introduscael primer numero: ");
                Num1 = Convert.ToInt32(Console.ReadLine());

                Console.WriteLine("Introdusca el segundo numero: ");
                Num2 = Convert.ToInt32(Console.ReadLine());

                if (Num1 > Num2)
                {
                    int suma = Num1 + Num2;
                    int diferencia = Num1 - Num2;
                    Console.WriteLine($"La suma de los numeros es: {suma}");
                    Console.WriteLine($"La diferencia de los numeros es: {diferencia}");
                }
                else
                {
                    int producto = Num1 * Num2;
                    decimal division = 0;
                    division = (decimal)Num1 / Num2;
                    Console.WriteLine($"El producto de los numeros es: {producto}");
                    Console.WriteLine($"La division de los numeros es: {division}");
                  
                }
            }
            catch (FormatException ex)
            {
                Console.WriteLine($"Error: Introdusca un numero valido: {ex.Message}");
            
            }
            catch (Exception ex)
            {
                Console.WriteLine($"Ocurrio un error: {ex.Message}");
            }
        }
    }
}
