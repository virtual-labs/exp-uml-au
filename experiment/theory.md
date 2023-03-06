### Theory

**Class diagram**

* A class diagram depicts classes and their interrelationships.
* Used for describing structure and behavior in the use cases.
* Provide a conceptual model of the system in terms of entities and their relationships.
* Used for requirement capture, end-user interaction.

    * Detailed class diagrams are used for developers.

* Design of a class in class diagram:

    * A class is a description of a set of objects that share the same attributes, operations, relationships, and semantics. 
    * Graphically, a class is rendered as a rectangle, usually including its name, attributes, and operations in separate, designated compartments. 
    * The name of the class is the only required tag in the graphical representation of a class.  It always appears in the top-most compartment.
    * An attribute is a named property of a class that describes the object being modeled. In the class diagram, attributes appear in the second compartment just below the name-compartment.
        * Attributes are usually listed in the form:<br>attributeName : Type
        * attributes (fields, instance variables)<br>visibility name : type [count] = default_value<br>visibility:	+	public<br> #	protected<br>-	private<br>~	package (default)<br>/	derived
        * A derived attribute is one that can be computed from other attributes, but doesn’t actually exist. For example, a Person’s age can be computed from his birth date. A derived attribute is  designated by a preceding ‘/’ as in: <br> / age : Date
    * operations / methods (optional) describe the class behavior and appear in the third compartment. 
        * You can specify an operation by stating its signature: listing the name, type, and default value of all parameters, and, in the case of visibility name (parameters) : return_type<br>visibility:	+	public<br>#	protected<br>-	private<br>~	package (default)<br>underline static methods<br>parameter types listed as (name: type)<br>omit return_type on constructors and when return type is void<br>method example: + distance(p1: Point, p2: Point): double 
        * You may omit trivial (get/set) methods, but don't omit any methods from an interface!
        * It should not include inherited methods.<br> ![fig1](/experiment/images/fig_1.jpg)

* Relationships

    * In UML, object interconnections (logical or physical), are modeled as relationships. 
    * There are two kinds of relationships in UML:
        * Generalizations 
        * associations 
    * generalization (inheritance) relationships- an inheritance relationship
        * inheritance between classes
        * interface implementation
            * hierarchies drawn top-down with arrows pointing upward to parent
            * line/arrow styles differ, based on whether parent is a(n):
                * class: solid line, black arrow
                * abstract class:solid line, white arrow
                * interface: dashed line, white arrow
            * we often don't draw trivial / obvious generalization relationships, such as drawing the Object class as a parent ![fig2](/experiment/images/fig_2.jpg)
    * Associational relationships - a usage relationship
        * Represent relationship between instances of classes
        * Association has two ends
            1. . multiplicity 	(how many are used)
                * ⇒ 1 exactly
                * ⇒ 0, 1, or more
                * 2..4	⇒ between 2 and 4, inclusive
                * 3..*	⇒ 3 or more
            2. name 		(what relationship the objects have)
            3. navigability	(direction) <br>![fig3](/experiment/images/fig_3.jpg)<br> ![fig4](/experiment/images/fig_4.jpg)
    
    * aggregation: “has-a"
        * symbolized by a clear white diamond<br> ![fig4](/experiment/images/fig_5.jpg)
    
    * composition:”part-off” / "is entirely made of"
        * stronger version of aggregation
        * the parts live and die with the whole
        * symbolized by a black diamond <br> ![fig6](/experiment/images/fig_6.jpg)
    * dependency: "uses temporarily"
        * symbolized by dotted line
        * often is an implementation detail, not an intrinsic part of that object's state <br> ![fig7](/experiment/images/fig_7.jpg)
    * Aggregation implies a relationship where the child can exist independently of the parent.
    * Composition implies a relationship where the child cannot exist independent of the parent. 
    * Composition is a strong Association whereas Aggregation is a weak Association




* Types of Classes
    * Ones found during analysis (From Object Model):
        * people, places, events, and things about which the system will capture information
        * ones found in application domain.

    * Ones found during design:
        * specific objects like windows and forms that are used to build the system.











    


    


