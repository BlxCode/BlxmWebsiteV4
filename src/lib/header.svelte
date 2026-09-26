<script>
  import kakaRenderSrc from "$lib/assets/kakaReder.png";

  let selectedCard = $state("Idiot");
  let notSelectedCards = $state(["Developer", "YouTuber"]);
  let cardDescriptions = {
    Idiot:
      "There were many times when I was an idiot, but I learned from my mistakes and grew as a person.",
    Developer: "I am a 'developer' and I love to code. My GitHub is @BlxCode. I know many programming languages, but my favorite is Svelte.",
    YouTuber:
      "I am a very small YouTuber, but I love to create content. My YouTube channel is @bloxdmaster",
  };
  let cardMoves = {
    Idiot: "translateX(-60%)",
    Developer: "translateX(-10%)",
    YouTuber: "translateX(60%)",
  };
  const defaultButtonClasses =
    "animate-fadeInWait p-2 cursor-pointer hover:bg-blue-900 hover:scale-105 active:scale-95 active:bg-blue-950";

  function updateSelectedCard(card) {
    document.getElementById(selectedCard + "Button").classList =
      defaultButtonClasses;

    if (
      selectedCard === card &&
      document.getElementById("selectedCard").hidden === false
    ) {
      document.getElementById("selectedCard").hidden = true;
      document.getElementById(selectedCard + "Button").classList =
        defaultButtonClasses;
      return;
    }
    notSelectedCards.push(selectedCard);
    document.getElementById("selectedCard").hidden = false;

    selectedCard = card;
    notSelectedCards.indexOf(card) !== -1
      ? notSelectedCards.splice(notSelectedCards.indexOf(card), 1)
      : null;

    document.getElementById(card + "Button").classList.add(["bg-blue-900"]);
    document.getElementById("selectedCard").style.transform = cardMoves[card];
  }
</script>

<h1
id="top"
  class=" flex text-9xl font-medium text-center flex-wrap justify-center items-center gap-4 animate-fadeIn mb-0.5"
>
  I'm <span class="font-bold drop-shadow-[0px_0px_19px_rgba(0,17,255,0.7)]">
    Blxm
  </span>
  <img draggable="false" src={kakaRenderSrc} alt="Blxm Logo" class="w-50" />
</h1>
<div
  id="contact"
  class="text-center text-2xl font-medium animate-fadeInWait flex gap-20 justify-center items-center flex-wrap"
>
  <button
    id="IdiotButton"
    onclick={() => {
      updateSelectedCard("Idiot");
    }}
    class="animate-fadeInWait p-3 cursor-pointer hover:bg-blue-900 hover:scale-105 active:scale-95 underline"
    >Idiot</button
  >
  <button
    id="DeveloperButton"
    onclick={() => {
      updateSelectedCard("Developer");
    }}
    class="animate-fadeInWait p-3 cursor-pointer hover:bg-blue-900 hover:scale-105 active:scale-95 underline"
    >Developer</button
  >
  <button
    id="YouTuberButton"
    onclick={() => {
      updateSelectedCard("YouTuber");
    }}
    class="animate-fadeInWait p-3 cursor-pointer hover:bg-blue-900 hover:scale-105 active:scale-95 underline"
    >YouTuber</button
  >
</div>

<div
  id="selectedCard"
  class="bg-blue-900 text-center w-80 mx-auto p-5 transition-[transform] duration-150"
  style="transform: translateX(-60%) !important;"
  hidden
>
  <h2 class="text-3xl font-bold">{selectedCard}</h2>
  <p class="text-2xl">{cardDescriptions[selectedCard]}</p>
</div>
