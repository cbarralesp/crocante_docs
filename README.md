# crocante_docs

Material de clases del proyecto **Crocante** (Desarrollo de Software Web II, Instituto Profesional San Sebastián).

| Clase | Documento | Presentación |
|---|---|---|
| 1. Primer Controller con Swagger | [Clase 1 - Crocante.docx](clase-01/Clase%201%20-%20Crocante.docx) | [Clase 1 - Crocante.pptx](clase-01/Clase%201%20-%20Crocante.pptx) |

Código del proyecto:

- Backend: https://github.com/cbarralesp/crocante_backend (un tag de Git por paso: `paso-00` a `paso-05`)
- Frontend: https://github.com/cbarralesp/crocante_frontend

Los documentos usan las fuentes institucionales Montserrat y Gotham; sin ellas Word y PowerPoint muestran fuentes sustitutas.


Query para la db 


DO $$
BEGIN
   IF NOT EXISTS (SELECT FROM pg_roles WHERE rolname = 'crocante') THEN
      CREATE USER crocante WITH PASSWORD 'crocante';
   ELSE
      ALTER USER crocante WITH PASSWORD 'crocante';
   END IF;
END
$$;

GRANT ALL PRIVILEGES ON DATABASE crocante TO crocante;
GRANT ALL ON SCHEMA public TO crocante;


