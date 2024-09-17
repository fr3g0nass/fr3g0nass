public final class fr3g0nass extends GitHubUser {

  public fr3g0nass() {
    super("fr3g0nass", "Spain", 19);
    
    this.addLanguage(Language.JAVA); 
    this.addLearningLanguage(
      Language.JAVASCRIPT,
    );
    
    this.addExperience(
      "Spigot API",
      "Paper API",
    );
  }
}

public abstract class GitHubUser {

  @Getter private final String username;
  @Getter private final String country;
  @Getter private final int age;

  private final Set<String> experiences = new HashSet<>();
  private final Set<Language> languages = new HashSet<>();
  private final Set<Language> learningLanguage = new HashSet<>(); // General Languages

  public GitHubUser(
      String username, 
      String country, 
      int age
      
  ) {
  
      this.name = username;
      this.country = country;
      this.age = age:
  }

  public void addLanguage(
      Language... language
  ) {
      this.languages.addAll(language);
  }
  
  public void addExperience(
      String... experience
  ) {
      this.experiences.addAll(experience);
  }
  
  public void addLearningLanguage(
      Language... languages
  ){
      this.learningLanguage.addAll(languages);
  } 
}

public enum Language {

  HTML,
  CSS,
  JAVA,
  JAVASCRIPT,
  PYTHON,
  PHP,

}
