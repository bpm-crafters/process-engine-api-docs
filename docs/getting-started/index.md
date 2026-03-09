If you want to try out `process-engine-api` library in your project, there are two steps you need to perform.

First, add the library to your project classpath. In Apache Maven it is just adding the following dependency into your 
project's `pom.xml`:

```xml 
  <dependency>
    <groupId>dev.bpm-crafters.process-engine-api</groupId>
    <artifactId>process-engine-api</artifactId>
    <version>${process-engine-api.version}</version>
  </dependency>
```

This dependency provides you with the most important classes required for implementation of your system using
a process engine. Here is an example of how a user task can be completed:

```java

import dev.bpmcrafters.processengineapi.task.*;

@Component
@RequiredArgsConstructor
@Slf4j
public class CompleteUserTaskUseCase implements CompleteUserTaskInPort {

  private final UserTaskCompletionApi taskCompletionApi;

  @Override
  public void completeUserTaskWithSomeValue(String taskId, String value) {
    taskCompletionApi.completeTask(
      new CompleteTaskCmd(
        taskId,
        () -> Map.of("some-user-value", value)
      )
    ).get();
  }

}

```

As you can see, the code above doesn't contain any engine-specific code, but rather uses only code from `process-engine-api`.
This means that the resulting code is portable and the decision about the used engine doesn't influence the implementation
of your application logic.

The second step depends on your target architecture and used process engine. Please check the quickstart sections of the available adapters.
