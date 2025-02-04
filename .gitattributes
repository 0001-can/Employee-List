using System;
using System.Collections.Generic;


class Employee
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string Last_Name { get; set; }
    public string Positation { get; set; }
    public string Importance_Level { get; set; }//-Low,Medium,High,Critical-four level between
    public double Salary { get; set; }
}
class Program
{
    static List<Employee> employees = new List<Employee>();
    static int currentId = 1;
    static void Main(string[]args)
    {
        while (true)
        {
            Console.WriteLine("\n Personel yönetim sistemi");
            Console.WriteLine("1-Çalışan ekle");
            Console.WriteLine("2-Çalışanı düzenle");
            Console.WriteLine("3-Çalışanı sil");
            Console.WriteLine("4-Çalışanları  listele");
            Console.WriteLine("5-Çıkış");
            Console.Write("Seçim  = ");
            string choice = Console.ReadLine();
            switch (choice)
            {
                case "1":
                    AddEmployee();
                    break;
                case "2":
                    EditEmployee();
                    break;
                case "3":
                    DeleteEmployee();
                    break;
                case "4":
                    ListEmployees();
                    break;
                case "5":
                    return;
                default:
                    Console.WriteLine("Geçersiz seçim! Tekrar deneyin.");
                    break;
            }
             }
    }
static void AddEmployee()
    {
        Employee employee = new Employee();
        employee.Id = currentId++;
        Console.Write("Çalışan Adı= ");
        employee.Name = Console.ReadLine();
        Console.Write("Çalışan Soyadı=  ");
        employee.Last_Name = Console.ReadLine();
        Console.Write("Çalışanın Pozisyonu=");
        employee.Positation = Console.ReadLine();
        Console.Write("Çalışanın Pozisyonunun Önem Seviyesi= ");
        employee.Importance_Level = Console.ReadLine();
        Console.Write("Çalışanın Maaşı=");
        if(double.TryParse(Console.ReadLine(),out double salary))
        {
            employee.Salary = salary;
        }
        else
        {
            Console.WriteLine("Geçersiz Maaş Değeri.Direk 0 olarak ayarlandı.");
            employee.Salary = 0;
        }
        employees.Add(employee);
        Console.WriteLine("Yeni Çalışan eklendi");
                }
    static void EditEmployee()
    {
        Console.Write("Düzenlemek İstediğiniz çalışanın Id'sini girin= ");
        if (int.TryParse(Console.ReadLine(), out int id))
        {
            Employee employee = employees.Find(e => e.Id == id);
            if (employee != null)
            {
                Console.Write("Yeni Ad=");
                employee.Name = Console.ReadLine();
                Console.Write("Yeni Soyad=");
                employee.Last_Name = Console.ReadLine();
                Console.Write("Yeni Pozisyon=");
                employee.Positation = Console.ReadLine();
                Console.Write("Yeni Pozisyon Önem Düzeyi=");
                employee.Importance_Level = Console.ReadLine();
                Console.Write("Yeni Maaş=");
                if (double.TryParse(Console.ReadLine(), out double salary))
                {
                    employee.Salary = salary;
                }
                else
                {
                    Console.WriteLine("Geçersiz Maaş değeri.");
                }
                Console.WriteLine("Çalışan düzenlendi.");

            }
            else
            {
                Console.WriteLine("Çalışan Bulunamadı ! ");
            }
        }
        else
        {
            Console.WriteLine("Geçersiz Id!");
        }
    }
   static void DeleteEmployee()
    {
        Console.Write("Silmek İstediğiniz Çalışanın Id'si girin= ");
        if (int.TryParse(Console.ReadLine(),out int id))
        {
            Employee employee = employees.Find(e => e.Id == id);
            if (employee!=null)
            {
                employees.Remove(employee);
                Console.WriteLine("Çalışan Silindi.");
                 }
            else
            {
                Console.WriteLine("Çalışan Bulunamadı!");
            }
        }
    else
        {
            Console.WriteLine("Geçersiz Id ! ");
        }
    
    }
    
    static void ListEmployees()
    {
        Console.WriteLine("\n Çalışanlar = ");
        foreach(var employee in employees)
        {
            Console.WriteLine("Id={0} Ad={1} Soyad={2} Pozisyon={3} Pozisyonunun Önem Seviyesi={4} Maaş={5}", employee.Id, employee.Name, employee.Last_Name, employee.Positation, employee.Importance_Level, employee.Salary);
        }
    }








}
