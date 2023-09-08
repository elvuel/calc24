<script context="module">
  //@ts-nocheck
  const seedDeck = () => {
    const suits = ["spade", "heart", "club", "diamond"];
    const ranks = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13];
    const deck = [];

    // Add standard 52 cards
    for (const suit of suits) {
      for (const rank of ranks) {
        deck.push({ suit, rank });
      }
    }

    return deck;
  };

  const shuffleDeck = (deck) => {
    for (let i = deck.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [deck[i], deck[j]] = [deck[j], deck[i]];
    }
  };
</script>

<script>
  //@ts-nocheck
  import Number from "$lib/components/Number.svelte";
  import { calc24 } from "$lib/calc24";

  let cards = [];

  let shownCards = [];

  let gameStarted = false;

  let tips = [];
  let tipsShow = false;

  const start = () => {
    cards = seedDeck();
    shuffleDeck(cards);
    // pop 4 cards to show
    shownCards = cards.splice(0, 4);
  };

  const round = () => {
    if (cards.length < 4) {
      cards = seedDeck();
      shuffleDeck(cards);
    }
    shownCards = cards.splice(0, 4);
  };

  const checkTips = () => {
    const numbers = shownCards.map((item) => item.rank);
    const valids = calc24(...numbers);
    tips = valids;
    tipsShow = true;
  };

  const closeTips = () => {
    tips = [];
    tipsShow = false;
  };
</script>

{#if tipsShow}
  <div
    class="absolute top-0 right-0 max-w-[200px] min-w-[200px] shadow-inner h-full bg-yellow-100 p-2"
  >
    <div class="grid place-items-center">
      <div class="flex flex-col mb-5">
        <button
          type="button"
          class="btn variant-filled btn-sm"
          on:click|preventDefault={() => {
            closeTips();
          }}>关闭提示</button
        >
      </div>
      <div
        class="max-h-[600px] min-h-[300px] flex flex-col gap-4 text-[1.125rem] overflow-y-auto font-semibold p-2"
      >
        {#if tips.length === 0}
          <div class="text-red-500 font-bold">无解</div>
        {:else}
          {#each tips as tip}
            <div class=" text-blue-500">
              {tip}
            </div>
          {/each}
        {/if}
      </div>
    </div>
  </div>
{/if}

<div class="grid h-screen place-items-center bg-white">
  <div class="flex flex-col gap-4">
    <div class>
      <h1
        class="text-4xl font-bold text-center text-gray-800 border-b-4 border-solid border-gray-400"
      >
        24点游戏
      </h1>
    </div>
    <div class="flex flex-row gap-3">
      {#if shownCards.length == 4}
        {#each shownCards as card}
          <Number number={card.rank} suit={card.suit} />
        {/each}
      {:else}
        <Number number={0} />
        <Number number={0} />
        <Number number={0} />
        <Number number={0} />
      {/if}
    </div>
    <div class="grid place-items-center">
      <div class=" flex flex-row gap-5">
        {#if !gameStarted}
          <button
            type="button"
            class="btn variant-filled"
            on:click|preventDefault={(e) => {
              start();
              gameStarted = true;
            }}>开始</button
          >{/if}
        {#if gameStarted}
          <button
            type="button"
            class="btn variant-filled"
            on:click|preventDefault={() => {
              round();
              closeTips();
            }}>换一组</button
          >
          <button
            type="button"
            class="btn variant-filled"
            on:click|preventDefault={() => {
              checkTips();
            }}>提示</button
          >
        {/if}
      </div>
    </div>
  </div>
</div>
