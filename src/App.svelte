<script>
import Header from "@/components/Header.svelte"
import Card from "@/components/Card.svelte"

const emojis = ['🥔', '🍒', '🥑', '🌽', '🥕', '🍇', '🍉', '🍌', '🥭', '🍍']
const gridSize = 4 // 4x4, 6x6
let cards = $state([])

function pickRandomEmojis() {
  const clonedEmojis = [...emojis]
  const randomEmojis = []
  const length = (gridSize * gridSize) / 2
  for (let i = 1; i <= length; i++) {
    const index = Math.floor(Math.random() * clonedEmojis.length)
    randomEmojis.push(clonedEmojis[index])
    clonedEmojis.splice(index, 1)
  }
  return randomEmojis
}

function shuffleEmojis() {
  const randomEmojis = pickRandomEmojis()
  cards = [...randomEmojis, ...randomEmojis]
  for (let i = cards.length - 1; i > 0; i--) {
    let index = Math.floor(Math.random() * i)
    const temp = cards[index]
    cards[index] = cards[i]
    cards[i] = temp
  }
}

shuffleEmojis()
</script>

<main class="main">
  <Header />
  <Card />
</main>

<style lang="scss">
  .main {
    width: 1200px;
    padding: 10px;
  }
</style>
