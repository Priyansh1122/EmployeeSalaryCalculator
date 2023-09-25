import java.util.ArrayList;

class Employee {
    String name;
    String gender;
    int age;
    double salary;

    public Employee(String name, String gender, int age, double salary) {
        this.name = name;
        this.gender = gender;
        this.age = age;
        this.salary = salary;
    }
}

public class EmployeeSalaryCalculator {
    public static void main(String[] args) {
        ArrayList<Employee> employees = new ArrayList<>();

        
        employees.add(new Employee("Aman", "Male", 24, 23000));
        employees.add(new Employee("Diksha", "Female", 22, 24000));
        employees.add(new Employee("Gaurav", "Male", 25, 30000));
        employees.add(new Employee("Kirti", "Female", 30, 40000));
        employees.add(new Employee("Akash", "Male", 26, 34000));

        
        double totalSalary = 0;
        for (Employee employee : employees) {
            totalSalary += employee.salary;
        }
        double averageTotalSalary = totalSalary / employees.size();

        
        double maleTotalSalary = 0;
        int maleCount = 0;
        for (Employee employee : employees) {
            if (employee.gender.equals("Male")) {
                maleTotalSalary += employee.salary;
                maleCount++;
            }
        }
        double averageMaleSalary = maleTotalSalary / maleCount;

        
        double femaleTotalSalary = 0;
        int femaleCount = 0;
        for (Employee employee : employees) {
            if (employee.gender.equals("Female")) {
                femaleTotalSalary += employee.salary;
                femaleCount++;
            }
        }
        double averageFemaleSalary = femaleTotalSalary / femaleCount;

        
        System.out.println("Average Total Salary for All Employees: " + averageTotalSalary);
        System.out.println("Average Total Salary for Male Employees: " + averageMaleSalary);
        System.out.println("Average Total Salary for Female Employees: " + averageFemaleSalary);
    }
}
