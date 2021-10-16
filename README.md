# AbstractFactoryPatternHW
This is my homework for the Software Design Patterns Discipline.

After a bit of thought, i have finally come up with an example for Abstract Factory Pattern as the School as for liberal arts and as for Technical School.

First of all, i have created interfaces such as Teacher, School Principal, Tutor which consists methods they perform in their work.
For instance, for Teacher interface, Teacher teaches students.

Then i have created Factory Interface which consists get methods such as getTeacher(), getTutor(), getPrincipal().

After that i have created two packages, as for technical school and as for Humanitarian School for a comfortable distribution of classes.
In each of them, i have implemented several classes for our interfaces. For example, we can take English Teacher which implements Teacher interface and implements teach method. And for each of them, I distributed each assigned task.

On the main class, we output each of them.

public class Main {
    public static void main(String[] args) {
        SchoolFactory schoolFactory = new TechnicanSchool();
        Teacher teacher = schoolFactory.getTeacher();
        PrincipalSchool principalSchool = schoolFactory.getPrincipal();
        Tutor tutor = schoolFactory.getTutor();

        System.out.println("This is the technical school...");
        teacher.teach();
        principalSchool.manage();
        tutor.prepare();
    }
    
    Output:
    
This is the technical school...
Teacher teaches math to the students
School Principal managaes Technical School
Technical tutor prepare for physics/math olympiads
