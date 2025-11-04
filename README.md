# sesgos
El corpus fue elaborado manualmente y contiene 40 frases que describen comportamientos y características de estudiantes y docentes, equilibrando ejemplos positivos y negativos.
Las frases se repiten varias veces para reforzar el aprendizaje del modelo. Ejemplos positivos: “El estudiante es responsable y trabaja bien”, “La docente motiva al grupo y apoya el aprendizaje.” Pero también se utilizaron ejemplos negativos tales como: “El estudiante es vago y no participa” ,“El profesor no escucha a sus alumnos y llega tarde.”
Se observa una tendencia a asociar el rol “estudiante” con valores de esfuerzo, compromiso y responsabilidad.
El rol “docente” aparece vinculado con guía, apoyo y motivación, aunque también con frases críticas.
La proporción de frases positivas y negativas permite explorar cómo los modelos de lenguaje internalizan juicios de valor.
Se eligieron las siguientes palabras con carga emocional o valorativa: Palabra, estudiante, docente, responsable, vago, esfuerzo, irresponsable, colabora, compromiso, respeto y actitud. 
Tras entrenar el modelo (vector_size=50) y reducir la dimensionalidad con PCA (n_components=2), se genera un mapa semántico donde cada punto representa una palabra.
Interpretación general: “Estudiante” aparece más cercano a “responsable”, “esfuerzo” y “compromiso”, lo que sugiere una asociación positiva dominante.
“Vago” e “irresponsable” forman un subgrupo negativo separado. Y por último “Docente” se ubica entre “respeto” y “colabora”, reflejando una visión de autoridad benevolente.
El embedding revela un sesgo valorativo hacia el estudiante “ideal”:
“Estudiante” tiende a vincularse más con virtudes que con defectos.
Los términos negativos (“vago”, “irresponsable”) quedan alejados, pero su presencia refuerza la idea de que “buen estudiante” = “responsable” y “malo” = “vago”.
El experimento demuestra que los modelos de PLN (Procesamiento de Lenguaje Natural) no son neutrales:
aprenden los sesgos implícitos en el lenguaje humano.
Por qué es un problema en noticias o medios: Si un modelo se entrena con noticias que describen a ciertos grupos sociales o profesiones con prejuicios, reproducirá esos estereotipos. Puede influir en sistemas automáticos de recomendación, evaluación o selección (por ejemplo, asociar “mujer” con “enfermera” y “hombre” con “ingeniero”).
Efectos en la audiencia: Refuerza percepciones injustas o discriminatorias, reduce la diversidad de representaciones sociales.
Propuestas para un uso responsable:
Analizar los corpus antes del entrenamiento (auditoría de sesgos), aumentar la diversidad temática y demográfica de los textos, aplicar técnicas de de-biasing o neutralización de embeddings y promover la alfabetización digital crítica: enseñar a los usuarios que la IA aprende de nosotros.
Como finalización cabe desatacar que el ejercicio muestra cómo Word2Vec refleja fielmente los patrones culturales del lenguaje.
Por tanto, la responsabilidad ética recae en quién diseña, selecciona y valida los datos.
Solo un uso consciente y supervisado del PLN puede evitar que la tecnología refuerce injusticias sociales.
