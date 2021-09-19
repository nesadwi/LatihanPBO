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
//Class Main
