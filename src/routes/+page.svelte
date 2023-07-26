<script>
  import { createMachine, interpret } from "xstate";

  const machine = createMachine({
    initial: "start",
    states: {
      start: {
        after: {
          // If this is uncommented, the subscription will work.
          // It is only the initial state of the machine that is not working.
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