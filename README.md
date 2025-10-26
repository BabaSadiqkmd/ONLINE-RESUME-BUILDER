Online Resume Builder (Spring Boot + Vaadin)

A Java-only web app to create resumes with personal details, skills, and certificate uploads. Built with Spring Boot, Vaadin (Java UI), Spring Data JPA, and H2.

Prerequisites
- Java 17+ (JDK installed and on PATH)
- Maven 3.9+ (optional; otherwise use your IDE to run Spring Boot)

Run
- If Maven is installed:
  - Command: mvn spring-boot:run
  - Open: http://localhost:8080/
- If Maven is NOT installed:
  - Import the project into IntelliJ IDEA or VS Code (Java extension)
  - Run class: com.resume.OnlineResumeBuilderApplication

Features
- Enter name, email, phone, summary
- Add skills (name, level)
- Upload certificates (stored under certificates/ on disk)
- Data persisted in H2 (./data/resume-db)
- REST: GET /api/resumes/{id} returns saved resume JSON

Configuration
- H2 console: /h2-console (JDBC URL: jdbc:h2:file:./data/resume-db)
- File storage root: app.storage.location in src/main/resources/application.properties

Build
- Command: mvn -DskipTests package

Notes
- First run will create certificates/ and ./data/ directories.
- Vaadin dev mode will auto-open your browser (configurable via application.properties).


