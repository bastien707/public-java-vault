- We can autowired in spring by **field**, **setter** or **constructor**
- Constructor is recommended because does not use [[Java Reflection API|reflection API]] which is expensive.

### By constructor  (*recommended*)
```java
public class UserService {
    private final UserRepository userRepository;
    
    public UserService(UserRepository userRepository) {
        this.userRepository = userRepository;
    }
}
```

Spring n'a pas besoin de réflexion ici car :

- Il utilise directement l'API Java standard pour créer l'objet
- Il appelle simplement `new UserService(userRepository)`
- Les paramètres sont passés directement au constructeur lors de l'instantiation
- C'est comme si on écrivait le code nous-mêmes

### By Field

```java
public class UserService {
    @Autowired
    private UserRepository userRepository;  // Private field !
}
```

Spring doit utiliser la réflexion car :

- L'objet est d'abord créé (via le constructeur par défaut)
- Puis [[Spring Framework 🌱|Spring]] doit accéder au champ `userRepository` qui est **privé**
- La seule façon d'injecter une valeur dans un champ privé est d'utiliser la [[Java Reflection API|réflexion]].


[[Beans]]
