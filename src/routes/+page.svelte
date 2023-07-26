<script>
  import { createMachine, interpret } from "xstate";

  const machine = createMachine({
    initial: "start",
    states: {
      start: {
        after: {
          // 500: {
          // }
        }
      }
    }
  });

  const myActor = interpret(machine).start();
</script>

<main>
  {JSON.stringify($myActor)}
</main>