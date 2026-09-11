import { useState, useMemo, useCallback } from "react";

/* ──────────── DATA ──────────── */
// Format: [questionText, [options], correctIndex]

const EXAMS = {
  "2-primaria": {
    "Lenguaje": [
      ["¿En cuál de las siguientes opciones TODAS las letras son vocales?", ["a, e, p, u", "e, i, o, u", "a, o, m, e"], 1],
      ["Si dividimos correctamente en sílabas la palabra \"mariposa\" (ma-ri-po-sa), ¿cuántas sílabas tiene?", ["3 sílabas", "4 sílabas", "5 sílabas"], 1],
      ["Identifica la vocal con la que inicia la palabra \"Avión\" y la letra final de la palabra \"Helado\":", ["Inicia con A, termina con O", "Inicia con E, termina con A", "Inicia con I, termina con O"], 0],
      ["¿Cuál de las siguientes sílabas falta para completar la palabra del animal saltarín: \"Ra - ____ - na\"?", ["ta", "to", "te"], 0],
      ["¿Qué sonido exacto se forma al unir la consonante \"m\" con las vocales \"o\" y \"a\" en ese orden?", ["mo - ma", "me - mo", "ma - mo"], 0],
      ["¿Cuántas letras en total tiene la palabra \"sol\" y cuántas vocales contiene?", ["3 letras y 2 vocales", "3 letras y 1 vocal", "4 letras y 1 vocal"], 1],
      ["Selecciona la opción que contiene únicamente palabras de 3 sílabas (trisílabas):", ["sol, perro, pan", "caracol, estrella, camisa", "mariposa, helicóptero, luz"], 1],
      ["Marca la palabra que comience con la consonante \"s\" y termine con la vocal \"a\":", ["Sombrero", "Sopa", "Sol"], 1],
      ["¿Cuál es el artículo determinado que corresponde a la palabra \"manzana\"?", ["El manzana", "La manzana", "Los manzana"], 1],
      ["De acuerdo con la regla de uso de mayúsculas en nombres propios, ¿cómo debe escribirse el nombre de una persona?", ["juan (todo minúscula)", "JUAN (todo mayúscula)", "Juan (primera letra mayúscula)"], 2],
      ["¿Cuál es la regla correcta para formar el plural de las palabras que terminan en \"z\", como \"lápiz\"?", ["Se cambia la Z por C y se agrega \"es\" (lápices)", "Se mantiene la Z y se agrega \"s\" (lápizs)", "Se escribe con Z y \"es\" (lápizes)"], 0],
      ["La letra \"H\" es muda en español. Identifica la palabra redactada correctamente con \"H\":", ["elado", "helado", "eladoh"], 1],
      ["Observa la frase: \"¿Cuál es tu animal favorito?\". ¿Qué signos se usan para realizar preguntas?", ["Signos de admiración ( ¡ ! )", "Signos de interrogación ( ¿ ? )", "Punto y coma ( ; )"], 1],
      ["Distingue la palabra que está escrita con la ortografía correcta:", ["Vaca (con V)", "Baka (con B y K)", "Vaka (con V y K)"], 0],
      ["¿Qué signo ortográfico es obligatorio colocar al finalizar toda oración?", ["Una coma ( , )", "Un punto ( . )", "Un guión ( - )"], 1],
      ["¿Por qué se dice que la letra \"H\" es una letra especial en el idioma español?", ["Porque suena como la letra S", "Porque es una letra muda (no tiene sonido propio)", "Porque siempre se escribe al final de las palabras"], 1],
      ["Dos palabras riman cuando terminan con el mismo sonido. ¿Cuál rima con \"gato\"?", ["Pato", "Perro", "Ratón"], 0],
      ["Lee la oración: \"El perro corre en el parque\". ¿Quién es el sujeto que realiza la acción de correr?", ["corre", "el parque", "El perro"], 2],
      ["Los antónimos son palabras con significados opuestos. ¿Cuál es el antónimo de la palabra \"día\"?", ["Sol", "Noche", "Luz"], 1],
      ["¿Cuál es la forma en femenino de la palabra \"león\"?", ["Leona", "Leoncita", "Leonera"], 0],
      ["Una sílaba trabada se compone de dos consonantes seguidas de una vocal. Encuentra la palabra con sílaba trabada:", ["Flor (fl)", "Mesa (m)", "Cama (c)"], 0],
      ["Los sinónimos son palabras que significan lo mismo. ¿Cuál es el sinónimo de la palabra \"pequeño\"?", ["Grande", "Chico", "Alto"], 1],
      ["Si completas \"_ato\" con la consonante \"g\", obtienes \"gato\". ¿Qué animal se forma si la completas con \"p\"?", ["Rato", "Pato", "Mato"], 1],
      ["Clasificación semántica: ¿Cuál de las siguientes palabras corresponde a la categoría de un COLOR?", ["Dulce", "Rojo", "Salado"], 1],
      ["Encuentra la pareja de palabras que tienen rima consonante perfecta al terminar en \"-ón\":", ["Camión y Avión", "Camión y Casa", "Camión y Flor"], 0],
    ]
  },
  "olimpiadas": {
    "Ciencias Sociales": [
      ["La conquista española provocó grandes cambios en la vida de los pueblos originarios.", ["Verdadero", "Falso"], 0],
      ["Durante la época colonial, todos los grupos sociales tenían los mismos derechos.", ["Verdadero", "Falso"], 1],
      ["Los pueblos indígenas realizaron diferentes rebeliones contra el dominio colonial.", ["Verdadero", "Falso"], 0],
      ["La independencia del Alto Perú se logró de un día para otro y sin luchas.", ["Verdadero", "Falso"], 1],
      ["La Guerra del Acre estuvo relacionada con la disputa por un territorio rico en recursos naturales, especialmente la goma.", ["Verdadero", "Falso"], 0],
      ["¿Qué ocurrió el 6 de agosto de 1825?", ["Se fundó la ciudad de La Paz", "Se declaró la independencia y nació Bolivia como país libre y soberano", "Se firmó un tratado de paz con España", "Se eligió al primer presidente"], 1],
      ["¿Cuál fue una de las funciones de la Primera Asamblea Constituyente?", ["Organizar el nuevo país", "Iniciar la conquista española", "Declarar la Guerra del Pacífico", "Entregar el territorio del Acre"], 0],
      ["¿Cómo se llamó inicialmente nuestro país después de su independencia?", ["Estado del Alto Perú", "República de Bolívar", "República del Acre", "Nueva España"], 1],
      ["¿Qué documento declaró oficialmente la independencia del nuevo país?", ["La Constitución Política", "El Acta de la Independencia", "El Tratado de Paz", "El Diario de Guerra"], 1],
      ["¿Quién fue el primer presidente de Bolivia?", ["Antonio José de Sucre", "Simón Bolívar", "Andrés de Santa Cruz", "Túpac Katari"], 0],
      ["¿Qué país ocupó el Litoral boliviano durante la Guerra del Pacífico?", ["Argentina", "Brasil", "Chile", "Perú"], 2],
      ["Bolivia nació como país independiente en el año 1825.", ["Verdadero", "Falso"], 0],
      ["Al inicio de la República, Bolivia tenía un territorio más extenso que el actual.", ["Verdadero", "Falso"], 0],
      ["La organización política de la República permitió establecer autoridades e instituciones para gobernar el país.", ["Verdadero", "Falso"], 0],
      ["En la época republicana, todas las personas tenían inmediatamente los mismos derechos y oportunidades.", ["Verdadero", "Falso"], 1],
      ["La Guerra del Pacífico ocasionó que Bolivia perdiera su salida soberana al océano Pacífico.", ["Verdadero", "Falso"], 0],
      ["¿Qué son los gobiernos autónomos departamentales?", ["Una institución que gobierna todo el país", "Una institución que ejerce autoridad en un departamento", "Una organización que administra empresas privadas", "Un grupo elegido para el congreso nacional"], 1],
      ["¿De qué se encargan los gobiernos autónomos departamentales?", ["De las relaciones internacionales", "De la administración de cada departamento y municipio", "De la defensa militar del territorio", "De la educación universitaria"], 1],
      ["¿Por qué los gobiernos departamentales son autónomos?", ["Porque no dependen de ninguna ley", "Porque cada departamento administra sus recursos económicos", "Porque eligen a su propio presidente", "Porque no pertenecen a Bolivia"], 1],
      ["¿Quién es el Gobernador actual de Cochabamba?", ["Evo Morales", "Leonardo Loza", "Luis Arce", "Manfred Reyes Villa"], 1],
      ["¿Qué son los recursos naturales?", ["Los productos fabricados en industrias", "Las riquezas que nos brinda la naturaleza", "Los bienes importados de otros países", "Las herramientas de trabajo agrícola"], 1],
      ["¿Cómo se clasifican los recursos naturales?", ["Grandes, medianos y pequeños", "Permanentes, renovables y no renovables", "Animales, vegetales y minerales", "Primarios y secundarios"], 1],
      ["¿Cuáles son recursos permanentes?", ["Las plantas y los animales", "Los minerales y los hidrocarburos", "El suelo, el agua, el aire y la energía solar", "La madera y el papel"], 2],
      ["¿Cuáles son ejemplos de recursos naturales renovables?", ["Los minerales y los hidrocarburos", "Las plantas y los animales", "El petróleo y el gas", "El oro y la plata"], 1],
      ["¿Cuáles son ejemplos de recursos naturales no renovables?", ["Las plantas y los animales", "El suelo y el agua", "Los minerales y los hidrocarburos", "La energía solar y el aire"], 2],
      ["¿Qué es el desarrollo sostenible?", ["Construir más fábricas rápidamente", "Cuidar los recursos naturales para la población actual y futura", "Explotar todos los recursos lo más rápido posible", "Importar recursos de otros países"], 1],
      ["¿Cómo se clasifican las actividades económicas?", ["Fáciles y difíciles", "Primarias, secundarias y terciarias", "Grandes y pequeñas", "Urbanas y rurales"], 1],
      ["¿Cuál de estas es una actividad económica primaria?", ["La fabricación de automóviles", "El turismo", "La agricultura", "El comercio en tiendas"], 2],
      ["¿En qué consiste la agricultura?", ["En la crianza de animales", "En el laboreo de los campos de cultivo", "En la extracción de minerales", "En la venta de productos"], 1],
      ["¿Qué mineral se produce en mayor cantidad en Bolivia?", ["El oro", "La plata", "El zinc", "El estaño"], 2],
      ["¿Qué fecha se recuerda como Día del Estado Plurinacional de Bolivia?", ["6 de agosto", "22 de enero", "1 de mayo", "25 de diciembre"], 1],
      ["¿Qué fecha se recuerda como Día del Mar?", ["12 de abril", "23 de marzo", "19 de marzo", "1 de mayo"], 1],
      ["¿Qué fecha se recuerda como Día del Niño en Bolivia?", ["25 de diciembre", "1 de junio", "12 de abril", "21 de septiembre"], 2],
      ["¿Qué fecha se recuerda como Día del Trabajo?", ["6 de agosto", "23 de marzo", "1 de mayo", "22 de enero"], 2],
      ["¿Qué fecha se recuerda como Día de la Madre en Bolivia?", ["8 de marzo", "27 de mayo", "12 de abril", "1 de mayo"], 1],
      ["¿Qué fecha se recuerda como Día del Maestro?", ["6 de junio", "6 de agosto", "21 de septiembre", "27 de mayo"], 0],
      ["¿Qué fecha se recuerda como Día de la Patria?", ["22 de enero", "23 de marzo", "6 de agosto", "17 de agosto"], 2],
      ["¿Qué fecha se recuerda como Día de la Bandera boliviana?", ["6 de agosto", "17 de agosto", "21 de septiembre", "22 de enero"], 1],
      ["¿Qué fecha se recuerda como Día del Estudiante?", ["12 de abril", "6 de junio", "21 de septiembre", "27 de mayo"], 2],
      ["¿Qué fecha se recuerda como Día del Padre?", ["19 de marzo", "27 de mayo", "6 de junio", "1 de mayo"], 0],
      ["¿Cuáles son danzas folklóricas de Cochabamba?", ["Morenada, Diablada y Tinku", "Caporales, Cueca cochabambina y Salaque", "Saya, Tobas y Kullawada", "Waca Waca, Llamerada y Pujllay"], 1],
      ["¿Bolivia solo tiene una danza folklórica?", ["Sí, solo tiene una danza nacional", "No, Bolivia tiene muchas danzas según cada región", "Sí, la Cueca es la única", "No tiene danzas propias"], 1],
      ["¿Cuáles son costumbres y tradiciones de Bolivia?", ["Halloween, Navidad y Año Nuevo", "Todos Santos, la Ch'alla y el Carnaval de Oruro", "Día de Acción de Gracias y San Valentín", "Oktoberfest y Pascua"], 1],
      ["¿Cuántas banderas ha tenido Bolivia a lo largo de su historia?", ["1 bandera", "2 banderas", "3 banderas", "4 banderas"], 2],
      ["¿Cuántas estrellas tenía el primer Escudo de Bolivia?", ["9 estrellas", "5 estrellas", "3 estrellas", "7 estrellas"], 1],
      ["¿Cuáles son las flores nacionales de Bolivia?", ["La rosa y el clavel", "La kantuta y el patujú", "La orquídea y el girasol", "El jazmín y la violeta"], 1],
      ["¿En qué año fue promulgada la actual Constitución Política del Estado boliviano?", ["2005", "2009", "2015", "2000"], 1],
      ["¿Cuántos artículos contiene la actual Constitución Política del Estado boliviano?", ["200 artículos", "300 artículos", "411 artículos", "500 artículos"], 2],
    ],
    "Lenguaje": [
      ["¿Qué es la comunicación?", ["Una forma de jugar", "El proceso de transmitir y recibir información", "Una forma de escribir solamente", "Un tipo de dibujo"], 1],
      ["¿Cuál es un elemento importante de la comunicación?", ["Emisor", "Cuaderno", "Regla", "Recreo"], 0],
      ["¿Qué es el lenguaje?", ["Un medio que utilizamos para comunicarnos y expresar ideas", "Un juego de palabras", "Una materia de matemática", "Un instrumento musical"], 0],
      ["La comunicación verbal se realiza principalmente mediante:", ["Dibujos", "Palabras orales o escritas", "Señales de tránsito solamente", "Gestos únicamente"], 1],
      ["¿Qué permitió la comunicación escrita?", ["Guardar y transmitir información a través del tiempo", "Solamente dibujar", "Hablar más fuerte", "Jugar con letras"], 0],
      ["Una de las primeras formas de escritura fue:", ["La escritura mediante dibujos y símbolos", "Los mensajes de celular", "El periódico", "El libro digital"], 0],
      ["¿Qué es un diario personal o íntimo?", ["Un periódico que leen todas las personas", "Un escrito donde una persona expresa sus experiencias y sentimientos", "Un libro de matemáticas", "Una carta comercial"], 1],
      ["¿Cuál de las siguientes palabras lleva tilde correctamente?", ["arbol", "lapiz", "fácilmente", "dificil"], 2],
      ["¿Qué invento permitió producir muchos libros y textos con mayor rapidez?", ["La imprenta", "El teléfono", "La televisión", "La radio"], 0],
      ["¿Cuál es la función principal de un periódico o diario?", ["Informar sobre acontecimientos y hechos", "Enseñar solamente matemáticas", "Contar únicamente cuentos", "Vender juguetes"], 0],
      ["¿Qué es la poesía?", ["Una forma de expresión artística mediante palabras", "Una noticia del periódico", "Una carta personal", "Una regla ortográfica"], 0],
      ["El lenguaje literario se caracteriza por:", ["Ser creativo y expresivo", "Usar solamente números", "No expresar sentimientos", "Dar únicamente órdenes"], 0],
      ["¿Qué significa declamar?", ["Leer rápidamente sin comprender", "Expresar un poema con emoción, entonación y gestos", "Copiar un texto", "Escribir una noticia"], 1],
      ["La comunicación permite transmitir ideas, sentimientos e información.", ["Verdadero", "Falso"], 0],
      ["La comunicación verbal utiliza únicamente gestos y movimientos.", ["Verdadero", "Falso"], 1],
      ["La escritura ayudó a conservar conocimientos y acontecimientos importantes.", ["Verdadero", "Falso"], 0],
      ["La imprenta permitió la difusión de libros, periódicos y otros textos.", ["Verdadero", "Falso"], 0],
      ["Un diario personal puede contener experiencias y sentimientos de una persona.", ["Verdadero", "Falso"], 0],
      ["¿Cómo se llama la persona que envía un mensaje en la comunicación?", ["Receptor", "Emisor", "Canal", "Código"], 1],
      ["¿Cómo se llama la persona que recibe el mensaje?", ["Emisor", "Receptor", "Mensaje", "Contexto"], 1],
      ["¿Cuáles son los componentes básicos de la comunicación?", ["Solo emisor y receptor", "Emisor, receptor, mensaje, código, canal y contexto", "Solo mensaje y canal", "Emisor y código"], 1],
      ["¿Qué es la abreviatura?", ["Una palabra larga", "El acortamiento en la escritura de una palabra", "Un sinónimo", "Un tipo de oración"], 1],
      ["¿Qué es la sigla?", ["Una palabra compuesta", "Cada una de las letras iniciales de un grupo de palabras", "Un tipo de verbo", "Una oración completa"], 1],
      ["¿Qué es la narración?", ["Una ecuación matemática", "El relato de hechos vividos o imaginados por una o varias personas", "Un tipo de dibujo", "Una regla ortográfica"], 1],
      ["¿Cuáles son los cinco elementos de la narración?", ["Título, autor, fecha, lugar y hora", "Narrador, acciones, personajes, espacio y tiempo", "Inicio, medio, fin, autor y lector", "Sujeto, verbo, predicado, adjetivo y adverbio"], 1],
      ["¿Cuál es la estructura del cuento?", ["Inicio y final", "Introducción, nudo y desenlace", "Título, cuerpo y firma", "Saludo, desarrollo y despedida"], 1],
      ["¿Qué es el punto?", ["Un signo que separa palabras", "Un signo de puntuación que sirve para terminar una frase de sentido completo", "Un signo que indica pregunta", "Un adorno en la escritura"], 1],
      ["¿Qué son las narraciones ancestrales?", ["Noticias recientes de la televisión", "Narraciones antiguas difundidas a través del tiempo", "Historias inventadas ayer", "Informes científicos modernos"], 1],
      ["¿Qué es la leyenda?", ["Un poema moderno", "Narraciones transmitidas de generación en generación", "Una noticia del periódico", "Un informe escolar"], 1],
      ["En la oración: \"Manuel está feliz\". ¿Qué pronombre sustituye a Manuel?", ["Yo", "Ella", "Él", "Nosotros"], 2],
      ["¿Qué artículo va delante de \"auto\"?", ["La", "El", "Los", "Las"], 1],
      ["¿Cuáles son los dos tipos de artículos?", ["Grandes y pequeños", "Artículos definidos y artículos indefinidos", "Artículos largos y cortos", "Artículos simples y compuestos"], 1],
      ["¿Para qué sirve la coma?", ["Para terminar un texto", "Para hacer pequeñas pausas al leer un texto", "Para indicar una pregunta", "Para separar párrafos"], 1],
      ["¿Cuáles son las partes de una exposición?", ["Solo introducción y conclusión", "Introducción, desarrollo, conclusión y plenario", "Título y cuerpo", "Saludo y despedida"], 1],
      ["¿Cuál es el verbo en la siguiente oración: \"Los niños corren en el recreo\"?", ["niños", "recreo", "corren", "Los"], 2],
      ["¿Qué es un comunicado?", ["Un poema artístico", "Un informe que comunica información para conocimiento público", "Una carta personal", "Un cuento de hadas"], 1],
      ["¿Cuál es la diferencia entre publicidad y propaganda?", ["Son exactamente lo mismo", "La publicidad busca vender un producto, la propaganda busca influir en la actitud de la comunidad", "La publicidad es oral y la propaganda es escrita", "No existe diferencia alguna"], 1],
      ["¿Qué es un debate?", ["Una pelea entre personas", "Una discusión planificada y argumentativa", "Un monólogo individual", "Un tipo de cuento"], 1],
      ["¿Quiénes participan en un debate?", ["Solo el público", "El moderador y los participantes", "Solo una persona", "El escritor y el lector"], 1],
      ["¿Qué es el método Cornell?", ["Un tipo de examen", "Una técnica para tomar apuntes", "Un deporte", "Una forma de dibujar"], 1],
      ["¿Para qué sirve el mapa conceptual?", ["Para dibujar paisajes", "Para comprender un tema usando información visual y organizada", "Para escribir cartas", "Para hacer cálculos matemáticos"], 1],
      ["¿Cuáles son las partes reconocidas de una carta?", ["Solo saludo y despedida", "Fecha, destinatario, cargo, lugar, referencia, saludo, desarrollo, despedida y firma", "Solo el mensaje", "Título y autor"], 1],
      ["¿Cuándo se escribe con mayúscula?", ["Solo al inicio de un texto", "La primera letra de un escrito, después de punto, nombres propios y al iniciar citas textuales", "Nunca se usa mayúscula", "Solo en nombres de ciudades"], 1],
      ["¿Cuáles son las partes de una receta de cocina?", ["Solo los ingredientes", "Nombre del plato, tiempo de preparación, ingredientes e instrucciones", "Solo el nombre del plato", "Título y firma del chef"], 1],
    ]
  }
};

const COURSES = [
  { id: "2-primaria", label: "2° de Primaria" },
  { id: "olimpiadas", label: "4° de Primaria" },
];

/* ──────────── HELPERS ──────────── */
function shuffle(arr) {
  const a = [...arr];
  for (let i = a.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [a[i], a[j]] = [a[j], a[i]];
  }
  return a;
}

function prepareQuestions(raw) {
  return shuffle(raw).map(([q, opts, correct]) => {
    const correctText = opts[correct];
    const shuffled = shuffle(opts.map((o, i) => ({ text: o, orig: i })));
    return {
      question: q,
      options: shuffled.map(s => s.text),
      correctIndex: shuffled.findIndex(s => s.text === correctText),
    };
  });
}

/* ──────────── STYLES ──────────── */
const palette = {
  bg: "#F0F4FF",
  card: "#FFFFFF",
  primary: "#4F46E5",
  primaryLight: "#E0E7FF",
  primaryDark: "#3730A3",
  correct: "#16A34A",
  correctBg: "#DCFCE7",
  wrong: "#DC2626",
  wrongBg: "#FEE2E2",
  text: "#1E293B",
  muted: "#64748B",
  border: "#CBD5E1",
  accent: "#F59E0B",
  accentBg: "#FEF3C7",
};

export default function QuizApp() {
  const [screen, setScreen] = useState("start");
  const [courseId, setCourseId] = useState("");
  const [subject, setSubject] = useState("");
  const [questions, setQuestions] = useState([]);
  const [current, setCurrent] = useState(0);
  const [answers, setAnswers] = useState({});
  const [submitted, setSubmitted] = useState(false);

  const subjects = courseId ? Object.keys(EXAMS[courseId] || {}) : [];

  const startQuiz = useCallback(() => {
    if (!courseId || !subject) return;
    const raw = EXAMS[courseId][subject];
    setQuestions(prepareQuestions(raw));
    setAnswers({});
    setCurrent(0);
    setSubmitted(false);
    setScreen("quiz");
  }, [courseId, subject]);

  const selectAnswer = (qi, oi) => {
    if (submitted) return;
    setAnswers(prev => ({ ...prev, [qi]: oi }));
  };

  const finish = () => setSubmitted(true);

  const score = useMemo(() => {
    if (!submitted) return 0;
    return questions.reduce((s, q, i) => s + (answers[i] === q.correctIndex ? 1 : 0), 0);
  }, [submitted, questions, answers]);

  const wrongOnes = useMemo(() => {
    if (!submitted) return [];
    return questions
      .map((q, i) => ({ ...q, index: i, userAnswer: answers[i] }))
      .filter(q => q.userAnswer !== q.correctIndex);
  }, [submitted, questions, answers]);

  const restart = () => {
    setScreen("start");
    setCourseId("");
    setSubject("");
    setQuestions([]);
    setAnswers({});
    setSubmitted(false);
    setCurrent(0);
  };

  const retryQuiz = () => {
    const raw = EXAMS[courseId][subject];
    setQuestions(prepareQuestions(raw));
    setAnswers({});
    setCurrent(0);
    setSubmitted(false);
  };

  /* ─── START SCREEN ─── */
  if (screen === "start") {
    return (
      <div style={{ minHeight: "100vh", background: palette.bg, display: "flex", alignItems: "center", justifyContent: "center", padding: 16, fontFamily: "'Segoe UI', system-ui, -apple-system, sans-serif" }}>
        <div style={{ background: palette.card, borderRadius: 20, padding: "40px 32px", maxWidth: 440, width: "100%", boxShadow: "0 8px 32px rgba(79,70,229,0.12)" }}>
          <div style={{ textAlign: "center", marginBottom: 32 }}>
            <div style={{ fontSize: 48, marginBottom: 8 }}>📝</div>
            <h1 style={{ fontSize: 26, fontWeight: 700, color: palette.primary, margin: 0 }}>Olimpiadas Quiz</h1>
            <p style={{ color: palette.muted, fontSize: 14, marginTop: 6 }}>Selecciona tu curso y materia para comenzar</p>
          </div>

          <label style={{ display: "block", fontSize: 13, fontWeight: 600, color: palette.text, marginBottom: 6 }}>Curso</label>
          <div style={{ display: "flex", gap: 8, marginBottom: 20 }}>
            {COURSES.map(c => (
              <button
                key={c.id}
                onClick={() => { setCourseId(c.id); setSubject(""); }}
                style={{
                  flex: 1, padding: "12px 8px", borderRadius: 12, border: `2px solid ${courseId === c.id ? palette.primary : palette.border}`,
                  background: courseId === c.id ? palette.primaryLight : "white", color: courseId === c.id ? palette.primaryDark : palette.text,
                  fontWeight: 600, fontSize: 13, cursor: "pointer", transition: "all .15s"
                }}
              >{c.label}</button>
            ))}
          </div>

          {subjects.length > 0 && (
            <>
              <label style={{ display: "block", fontSize: 13, fontWeight: 600, color: palette.text, marginBottom: 6 }}>Materia</label>
              <div style={{ display: "flex", flexDirection: "column", gap: 8, marginBottom: 24 }}>
                {subjects.map(s => (
                  <button
                    key={s}
                    onClick={() => setSubject(s)}
                    style={{
                      padding: "12px 16px", borderRadius: 12, border: `2px solid ${subject === s ? palette.primary : palette.border}`,
                      background: subject === s ? palette.primaryLight : "white", color: subject === s ? palette.primaryDark : palette.text,
                      fontWeight: 600, fontSize: 14, cursor: "pointer", textAlign: "left", transition: "all .15s"
                    }}
                  >
                    {s === "Ciencias Sociales" ? "🌍 " : "📖 "}{s}
                    <span style={{ display: "block", fontSize: 11, fontWeight: 400, color: palette.muted, marginTop: 2 }}>
                      {EXAMS[courseId][s].length} preguntas
                    </span>
                  </button>
                ))}
              </div>
            </>
          )}

          <button
            onClick={startQuiz}
            disabled={!courseId || !subject}
            style={{
              width: "100%", padding: 14, borderRadius: 12, border: "none",
              background: (!courseId || !subject) ? palette.border : palette.primary,
              color: "white", fontWeight: 700, fontSize: 16, cursor: (!courseId || !subject) ? "default" : "pointer",
              transition: "all .15s"
            }}
          >Comenzar examen</button>
        </div>
      </div>
    );
  }

  /* ─── RESULTS SCREEN ─── */
  if (screen === "quiz" && submitted) {
    const pct = Math.round((score / questions.length) * 100);
    const emoji = pct >= 80 ? "🏆" : pct >= 60 ? "👍" : pct >= 40 ? "💪" : "📚";
    return (
      <div style={{ minHeight: "100vh", background: palette.bg, padding: 16, fontFamily: "'Segoe UI', system-ui, -apple-system, sans-serif" }}>
        <div style={{ maxWidth: 600, margin: "0 auto" }}>
          {/* Score card */}
          <div style={{ background: palette.card, borderRadius: 20, padding: "32px 24px", textAlign: "center", boxShadow: "0 8px 32px rgba(79,70,229,0.12)", marginBottom: 20 }}>
            <div style={{ fontSize: 56 }}>{emoji}</div>
            <h2 style={{ fontSize: 22, color: palette.text, margin: "8px 0 4px" }}>Resultados del examen</h2>
            <p style={{ color: palette.muted, fontSize: 13, margin: "0 0 20px" }}>{subject}</p>

            <div style={{ display: "inline-flex", alignItems: "baseline", gap: 4, background: pct >= 60 ? palette.correctBg : palette.wrongBg, padding: "16px 32px", borderRadius: 16 }}>
              <span style={{ fontSize: 48, fontWeight: 800, color: pct >= 60 ? palette.correct : palette.wrong }}>{score}</span>
              <span style={{ fontSize: 20, color: palette.muted }}>/ {questions.length}</span>
            </div>
            <p style={{ fontSize: 14, color: palette.muted, marginTop: 8 }}>{pct}% de aciertos</p>

            <div style={{ display: "flex", gap: 8, marginTop: 24 }}>
              <button onClick={retryQuiz} style={{ flex: 1, padding: 12, borderRadius: 12, border: `2px solid ${palette.primary}`, background: "white", color: palette.primary, fontWeight: 600, fontSize: 14, cursor: "pointer" }}>
                Reintentar
              </button>
              <button onClick={restart} style={{ flex: 1, padding: 12, borderRadius: 12, border: "none", background: palette.primary, color: "white", fontWeight: 600, fontSize: 14, cursor: "pointer" }}>
                Inicio
              </button>
            </div>
          </div>

          {/* Wrong answers */}
          {wrongOnes.length > 0 && (
            <div style={{ background: palette.card, borderRadius: 20, padding: "24px 20px", boxShadow: "0 4px 16px rgba(0,0,0,0.06)" }}>
              <h3 style={{ fontSize: 16, color: palette.wrong, margin: "0 0 16px", display: "flex", alignItems: "center", gap: 8 }}>
                <span>✗</span> Preguntas incorrectas ({wrongOnes.length})
              </h3>
              {wrongOnes.map((w, i) => (
                <div key={i} style={{ padding: "14px 0", borderTop: i > 0 ? `1px solid ${palette.border}` : "none" }}>
                  <p style={{ fontSize: 13, fontWeight: 600, color: palette.text, margin: "0 0 8px" }}>{w.question}</p>
                  {w.userAnswer !== undefined ? (
                    <p style={{ fontSize: 12, color: palette.wrong, margin: "0 0 4px", display: "flex", alignItems: "center", gap: 6 }}>
                      <span style={{ display: "inline-block", width: 16, height: 16, borderRadius: "50%", background: palette.wrongBg, textAlign: "center", lineHeight: "16px", fontSize: 10 }}>✗</span>
                      Tu respuesta: {w.options[w.userAnswer]}
                    </p>
                  ) : (
                    <p style={{ fontSize: 12, color: palette.muted, margin: "0 0 4px", fontStyle: "italic" }}>Sin respuesta</p>
                  )}
                  <p style={{ fontSize: 12, color: palette.correct, margin: 0, display: "flex", alignItems: "center", gap: 6 }}>
                    <span style={{ display: "inline-block", width: 16, height: 16, borderRadius: "50%", background: palette.correctBg, textAlign: "center", lineHeight: "16px", fontSize: 10 }}>✓</span>
                    Respuesta correcta: {w.options[w.correctIndex]}
                  </p>
                </div>
              ))}
            </div>
          )}
        </div>
      </div>
    );
  }

  /* ─── QUIZ SCREEN ─── */
  const q = questions[current];
  const totalQ = questions.length;
  const answered = Object.keys(answers).length;
  const progress = ((current + 1) / totalQ) * 100;

  return (
    <div style={{ minHeight: "100vh", background: palette.bg, padding: 16, fontFamily: "'Segoe UI', system-ui, -apple-system, sans-serif" }}>
      <div style={{ maxWidth: 600, margin: "0 auto" }}>
        {/* Header */}
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 12 }}>
          <span style={{ fontSize: 13, fontWeight: 600, color: palette.primary }}>{subject}</span>
          <span style={{ fontSize: 12, color: palette.muted }}>{answered}/{totalQ} respondidas</span>
        </div>

        {/* Progress bar */}
        <div style={{ height: 6, background: palette.primaryLight, borderRadius: 3, marginBottom: 20, overflow: "hidden" }}>
          <div style={{ height: "100%", width: `${progress}%`, background: palette.primary, borderRadius: 3, transition: "width .3s" }} />
        </div>

        {/* Question card */}
        <div style={{ background: palette.card, borderRadius: 20, padding: "28px 24px", boxShadow: "0 4px 20px rgba(79,70,229,0.08)", marginBottom: 16 }}>
          <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 16 }}>
            <span style={{
              display: "inline-flex", alignItems: "center", justifyContent: "center",
              width: 36, height: 36, borderRadius: "50%", background: palette.primaryLight,
              color: palette.primary, fontWeight: 700, fontSize: 14, flexShrink: 0
            }}>{current + 1}</span>
            <span style={{ fontSize: 12, color: palette.muted }}>de {totalQ}</span>
          </div>

          <p style={{ fontSize: 16, fontWeight: 600, color: palette.text, margin: "0 0 20px", lineHeight: 1.5 }}>{q.question}</p>

          <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
            {q.options.map((opt, oi) => {
              const selected = answers[current] === oi;
              return (
                <button
                  key={oi}
                  onClick={() => selectAnswer(current, oi)}
                  style={{
                    display: "flex", alignItems: "center", gap: 12,
                    padding: "14px 16px", borderRadius: 14,
                    border: `2px solid ${selected ? palette.primary : palette.border}`,
                    background: selected ? palette.primaryLight : "white",
                    color: palette.text, fontSize: 14, textAlign: "left",
                    cursor: "pointer", transition: "all .15s", lineHeight: 1.4
                  }}
                >
                  <span style={{
                    display: "inline-flex", alignItems: "center", justifyContent: "center",
                    width: 28, height: 28, borderRadius: "50%", flexShrink: 0,
                    border: `2px solid ${selected ? palette.primary : palette.border}`,
                    background: selected ? palette.primary : "white",
                    color: selected ? "white" : palette.muted,
                    fontSize: 12, fontWeight: 700
                  }}>
                    {String.fromCharCode(65 + oi)}
                  </span>
                  {opt}
                </button>
              );
            })}
          </div>
        </div>

        {/* Navigation */}
        <div style={{ display: "flex", gap: 8 }}>
          <button
            onClick={() => setCurrent(c => Math.max(0, c - 1))}
            disabled={current === 0}
            style={{
              flex: 1, padding: 13, borderRadius: 12, border: `2px solid ${palette.border}`,
              background: "white", color: current === 0 ? palette.border : palette.text,
              fontWeight: 600, fontSize: 14, cursor: current === 0 ? "default" : "pointer"
            }}
          >← Anterior</button>

          {current < totalQ - 1 ? (
            <button
              onClick={() => setCurrent(c => Math.min(totalQ - 1, c + 1))}
              style={{
                flex: 1, padding: 13, borderRadius: 12, border: "none",
                background: palette.primary, color: "white",
                fontWeight: 600, fontSize: 14, cursor: "pointer"
              }}
            >Siguiente →</button>
          ) : (
            <button
              onClick={finish}
              style={{
                flex: 1, padding: 13, borderRadius: 12, border: "none",
                background: palette.accent, color: "white",
                fontWeight: 600, fontSize: 14, cursor: "pointer"
              }}
            >Finalizar ✓</button>
          )}
        </div>

        {/* Question dots */}
        <div style={{ display: "flex", flexWrap: "wrap", gap: 6, justifyContent: "center", marginTop: 16, padding: "0 8px" }}>
          {questions.map((_, i) => (
            <button
              key={i}
              onClick={() => setCurrent(i)}
              style={{
                width: 28, height: 28, borderRadius: "50%", border: "none",
                fontSize: 10, fontWeight: 600, cursor: "pointer",
                background: i === current ? palette.primary : (answers[i] !== undefined ? palette.primaryLight : "#E2E8F0"),
                color: i === current ? "white" : (answers[i] !== undefined ? palette.primary : palette.muted),
              }}
            >{i + 1}</button>
          ))}
        </div>
      </div>
    </div>
  );
}
