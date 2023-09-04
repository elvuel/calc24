<script context="module">
  const SpadeIcon60 =
    "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAACXBIWXMAAAsTAAALEwEAmpwYAAACj0lEQVR4nO2ay2vUUBSHP+vCVwVxo3ahtr7Qon+FooJdiiji0pUoroT+AVoXIoLQhTsrFATxVavoRhdupIjga6+0CC6cUcv4GDty4QRCmGpycpOcDPeD36Izt8n5JsnNzb2BQCAQCAQitgOTwGfJpHzWcywBTgLfgU4iLeCMtOkJ1gMPuogmMwWso+YcllO3kzJf5EyoHQPAnQyiyTwENlKja/VrDtko88A5oA+jbAKeeBBN5rHFo30CaBYgG6Up+6ic5cCVAkWTuQ6srEp2G/CqRNko74DhsmX3FXwK/y8NYG9ZsseBXxXKRvkJHCta9gjQNiAbpV1kZzZiTDYufci37B7gmwG5xeIGOrt9yS4DXhuQStN7r/AhfNGATNqM5ZXdDPwwIJKl5x7MI3zNgETWjGtlV3l66ik7Te3w86iB4rVx44XMjBsoXJurGuEZA4Vr80IjPGegcG1mNcItA4Vr42rPTMNA4dq42c/MvDdQuDZvNMKPDBSuzbRG+KyBwrU5rR1Hd2oa9Xh6ykDxWXOXHOwEfhuQyDL7kXtGc8yASNqcxwNLPZ/a8TXibuvF2tz3uQ612pP0BPAs9vdT4IYn2X480wdcUM5cuiN5CtgKLMQ+/wNskdvIvGK7bTmNC11hHJZfNE1BTuiWSDkud2lzSb5zbW7L/6TZ9j1gFyUyKO9muFHNWxl7t+RJxY3SRoGhWPuhRebHWnLPJyY+KtuYle8bso9p2We8vVlu/uNoubd5eor9iWs3mQVZoOsJBoBPKa5JN+GwgZrTD7zM0OvOFHF7KYs1wHPlfNRaasYO6VXzPMDX5pXEEU9vBzSLWAYtgrmqZx/L5qNH4Q/UgIOepJ3sgaplAoFAIECJ/AVoaMZUPhK+UQAAAABJRU5ErkJggg==";
  const HeartIcon60 =
    "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAACXBIWXMAAAsTAAALEwEAmpwYAAACT0lEQVR4nO2aTUtUURjHf9OUueiF6Av4ErapZRDUor5Eu5AkcavZLogIAnHTLoKiRaVlGpRNoqh9ihALP0BvRJZDBWpx4BmQcJp7nnvOvY9yfvDfzTz3+TF3nnvuuRcSiUQikUjsRLqAIWAWWAJWgTqwDMwBg0CHom6n1J2TWnWpvSTHGpJjF8ZJ4DXwJ0M2gHGgJ0Pd48BT+U6W2jXgREzRKjDq0dDW/AKuAJVt6u4BhuUzvnXXgRHpLSgHPX7V/2UC2L+lbjswGaBuTXoMQjWQbCMzQJtkNmDdmpwtuRkN2FQj94D7Eeq60zv3gNqI0FisrOcdZDMGJHzzSivbbaB5bdy13JthA41r4xY93oScoEXH/RW9WTbQuDZuGerNqoHGtfmmEa4baFybNY3wioHGtXmnEV400Lg28xrh6wYa1+aaRvi0gca1OaURrgDvDTTvm5U8d01XDQj4xm0BqTkK/DAgkTXfgSPk5KYBkaxxgzY3B4APBmRa5VPIbZ5+A0Kt0kdAKsCCAalmedNkRzQXPUbX12uyWRGFAQOC/+YSkRk3INnIMwrgsNxgly37FjhEQXTKZaAs2S/AMQrmrPJ5UN78Bs5REr0lCF+mZEYKlL2FASrA3QJkH8RYXGhx95+PIso+DPVkMCTuseqTCLLPgb0YZR8wHVD2hdQ0TRswFUD2pbwhsCOoypDRyj62fBo3w03U2wrZOxYHlA83gM0MopuhtmgscAH42WK5eJFdxhng8zayX4Hz7FK6gDHgo2Ss6NcIE4lEIpFIUBp/AWE7uaAGP3e1AAAAAElFTkSuQmCC";
  const ClubIcon60 =
    "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAACXBIWXMAAAsTAAALEwEAmpwYAAACu0lEQVR4nO2azWsTQRiHn0NsPKtHRTzaVj2IIl4ERVGwVr2KKCKIFb0K/g9KQqr1YhWLxaMHBVHrRTz4gZcYPw9qRQ/ixURUjG1k4A0sy2SzOzPdZLb7wAslO++88wuz8/FLIScnJycnR7EOKAMvgZ8S6u8SMEyGKAKXgDmg1SH+AePAABkQ+zBCaDhmfBc9kUBsOyp4/M7OGQhW03sIDykbiG3HBTykZiG4ioc0LATX8ZC6heAfeMhbC8Gv8ZCbFoJv4CHHLAQfxUOWA78NxP4CluEp0waCr+MxmwwEb8RzHiQQe48MsD2B4G1khEcxxD6mzx2LBvAKmAQOAIWI3N0xBO+KyF8CHASuSs3GQjomxRiOhYpPwGkZnI5nEblPOuQoM+AMMNultjPHpJjQsVDxDhjV9HU4IueQpv1+4H3C2taOyYTBthJccQcDfS0FvmvafZMvts2g5JrWraTtWLQC0ZQvbY30eU3TRq0BSJvLkmNT09gxKVkWDgu/LZeC8DP12R0HQq0dk5rDAaQd1bQdi1aPo562Y9HqcRg5JrU+GHiqU7rkcAB/gVvAmObZmDzr+aI1LEu8rVB1Alotfa7StFkpz1Sbi462peD+n4hxi8J3gbWh/rZo2m0OtbE9eKjzvjEDCe+zKt4AIx36O6Jpr46cOvYZOJ/3I87yiURXYkzvD8DJLgXLCd831dcp4GOMaVx2ITbIkAyuKnt0XVbyK3JZiLoetnmuGezTGHkFuUxMSs26jEGN5bzNO7uQrOiwIDXF4cwcJyKm5HEyyEzWzbsg64H5CMHzWfvHlukYW8oUGWFDzNNTU0wHryl0Me/C8cL1Xpo25wyOhmfxlFHDi4DK2Yln7AD+GIgNXuC34gkjjuwhdXzciwd8dSC2HV/wgM8OBaufWPqePY5Ez8qPcDk5OTk5LBb+A1Uz44qlq69AAAAAAElFTkSuQmCC";
  const DiamondIcon60 =
    "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADwAAAA8CAYAAAA6/NlyAAAACXBIWXMAAAsTAAALEwEAmpwYAAAB+0lEQVR4nO2aSytFURiGH44Bym1GyElOBmYGZMBQymVmQgzkH0jJH3AUfoERoVwmLiV/QAoThDG5lEtHySUcnVprckL7OHuvtfZe+6l3snft1jNZ69vr+yAkJCTEOXXAGvAosiqeBZIY8AAk03Iv3gWKIuD4B1mZM6CUgJALbPwhK7MNRAgAkw5kZeL4nP4MZGWG8CmNwPM/hF+AZnxGOXDxD1mZK6AKn5AP7GYhK3MAFOIDZl2QlZnHcEZdlJVJfdNI2oEPD4Q/gS4Mo17UxkmP8gQ0YAjFwImHsjLnQJlu2QiwpUBWZgfI0yk8o1BWZlqX7KAGWZlh1bItwKtG4XegTZVsBXCpUVbmBqhWUTbuGSArc+hl+ZkDLBggmZ5VsTbXGTdA7rek1uYqHR6VjW6Wnz1uydYACQOknJSfUTeEFw2QcZrUWrPmxgARp7m1TfjKDeElA0ScJnVsZk1UbAhJw5MQG6w1x1I3FhUeY1hUWq54VVpa9/Ng2u/htcruRIvmC4A3oBXFDNh0xSOZ1iA7hebu/qZN17SqL+JLbWm1JExqtahopnViUbt0BIsa4nNYNPKwDxRg0VBLJRaNLTXhU3qBrwyF+/A58QxkJwgAucC6TcOlcnz46A/ZU6CEgBETw+DpsndBnoqvE+3NB5FloFb3okJCQvAN37r8CQXZujsLAAAAAElFTkSuQmCC";
</script>

<script>
  //@ts-nocheck
  export let number;
  export let suit = "spade";

  const suits = {
    spade: SpadeIcon60,
    heart: HeartIcon60,
    club: ClubIcon60,
    diamond: DiamondIcon60,
  };

  $: displayText =
    number < 1 || number > 13
      ? "..."
      : number === 1
      ? "A"
      : number === 11
      ? "J"
      : number === 12
      ? "Q"
      : number === 13
      ? "K"
      : number;
</script>

<div
  class="card p-10 bg-yellow-300 flex flex-col text-green-500 hover:text-red-500 font-bold text-[2rem] shadow-sm hover:shadow-2xl transition duration-500 ease-in-out transform hover:-translate-y-1 hover:scale-110"
>
  <div class="flex flex-col items-center gap-2">
    <div>
      <img src={suits[suit]} alt={`${suit} [${displayText}]`} />
    </div>
    <div>
      <span>{displayText}</span>
    </div>
  </div>
</div>
