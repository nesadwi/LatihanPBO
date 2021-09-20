// LATIHAN KMMI PBO KELOMPOK 4 
// Muhammad Wafa Al Ausath 2015061057
// Nesa Dwi Cahyani 2017051009

//Class Employee

abstract class Employee {
    private String name;
    private  String afm;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getAfm() {
        return afm;
    }

    public void setAfm(String afm) {
        this.afm = afm;
    }
    
    public abstract int payment();
}

//Class Hourly Employee
public class HourlyEmployee extends Employee{
    private int hoursWorked;
    private int hourlyPayment;

    public int getHoursWorked() {
        return hoursWorked;
    }

    public void setHoursWorked(int hoursWorked) {
        this.hoursWorked = hoursWorked;
    }

    public int getHourlyPayment() {
        return hourlyPayment;
    }

    public void setHourlyPayment(int hourlyPayment) {
        this.hourlyPayment = hourlyPayment;
    }
    
    @Override
    public int payment(){
        return this.getHourlyPayment() * this.getHoursWorked();
    }
}

//Class SalariedEmployee
public class SalariedEmployee extends Employee{
    private int salary;


    public void setSalary(int salary) {
        this.salary = salary;
    }

    public int getSalary() {
        return salary;
    }
    
    
    @Override
    public int payment(){
        return salary;
    }
}

//Class Main
public class Main {
    public static void main(String[] args) {
        
        
        SalariedEmployee salariedEmployee = new SalariedEmployee();
        HourlyEmployee hourlyEmployee = new HourlyEmployee();
        
        Employee[] employee = {salariedEmployee, hourlyEmployee};
        
        salariedEmployee.setName("hiji");
        salariedEmployee.setAfm("4234");
        salariedEmployee.setSalary(100);
        hourlyEmployee.setName("salari");
        hourlyEmployee.setAfm("1432");
        hourlyEmployee.setHoursWorked(8);
        hourlyEmployee.setHourlyPayment(10);
        
        for(int i = 0; i < 2; i++){
            System.out.println("Name : " + employee[i].getName());
            System.out.println("Payment: " + employee[i].payment());
            System.out.println();
        }
    }
}

// SCREENSHOT PROGRAM JAVA
![Class Main](https://user-images.githubusercontent.com/83526578/134005475-dd2c9f41-7d89-4833-913a-889d09d9ecb4.jpeg)
![Employee](https://user-images.githubusercontent.com/83526578/134005495-7804124e-e0a0-47cd-a678-7c9c18b686f5.jpeg)
![Hourly Employee](https://user-images.githubusercontent.com/83526578/134005519-44386fb5-69dd-4c47-b880-62ba8db848d2.jpeg)
![Salaried Employee](https://user-images.githubusercontent.com/83526578/134005546-bd39d5e2-c2fb-4b3e-b7f3-be1323ba1606.jpeg)
![Ouput](https://user-images.githubusercontent.com/83526578/134005569-fbac2e45-d44f-4e24-8ac8-ba94d058a76b.jpeg)
