# Web-development-2-Assignment-

Users / Meministrator / Deskiop / studentpromle api_ / student protlle apl / 
controlleconst Student = require(' ../models/Student');
const createStudent = async (req, res) =>
{try (const student = new Student (req. body) ;await student.save(); res. status (201)-json(student)
;} 
catch (error) {res. status (400) - json({ message: error.message });
const getAllStudents = async (req, res) → ( try (const students = avait Student.find();res.status (208).json(students);
} catch (error) {res.status(500). json({ message: error.message });}};
const updatestudent = async (req, res) => Etry fconst student = avait Student.findByIdAndUpdate(req.params.id, req.body, { new: true });
if (!student) return res. status (404) .json({ message: "Student not found" }); res.status (208). json(student);}
catch (error) €res.status (400) .json({ message: error.message });
const deleteStudent = async (reg, res) → { try fconst student = await Student.findByIdAndDelete(req.params.id);
if (Istudent) return res.status (404) json({ message: "Student not found" }); 
res.status (200). json({ message: "Student deleted successfully" });} catch (error) {res. status (500) json({ message: error-message });};module. exports = (createStudent, getAllStudents, getStudentById,updateStudent, deleteStudent,
