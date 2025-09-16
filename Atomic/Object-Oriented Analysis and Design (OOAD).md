OOA/D is about **seeing the world in terms of concepts**.

- Example (classroom): benches, students, teacher.
- Example (hospital): beds, patients, doctors.
- Example (zoo): animals, zookeepers, cages.

## Classes and Objects

- **Class** → blueprint for objects.
- **Object** → instance of a class.

Example in Python:

```python
class Teacher:     
	def __init__(self, name):
		self.name = name  

Deena = Teacher("Deena")
```

## Analysis vs Design vs Modelling

- **Analysis** → identify objects in the problem domain.
- **Design** → define how these objects become software.
- **Modelling** → visualise the problem and solution.

**Example Domain Model:**  
![[Domain Model.png]]

- Boxes = classes.
- Arrows = relations.
- Numbers on arrows = how many objects are involved.