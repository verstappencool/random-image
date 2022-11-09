<script>
  import Button from './lib/Button.svelte';
  import Image from './lib/Image.svelte';
  import Footer from './lib/Footer.svelte';
  import { getRandomImage } from './utils/getData';
  import { choices } from './utils/choices';
  import Check from './lib/Check.svelte';
  import Heading from './lib/Heading.svelte';

  let imageData;
  let isSfw = true;

  const onClick = () => {
    isSfw = !isSfw;
  };

  const changeImage = async (choice = 'blush') => {
    imageData = await getRandomImage(choice, isSfw);

    console.log(imageData);
  };

  changeImage();

  /**
   * @param {string} choice
   */
  function changeChoice(choice) {
    changeImage(choice);
  }
</script>

<Heading />

<main>
  <figure>
    <Image {imageData} />
  </figure>
  <section>
    <Button {choices} {changeChoice} />
    <Check {isSfw} {onClick} />
  </section>
  <Footer />
</main>
