<template>
  <div>
    <router-link to="/">home</router-link>
  </div>
</template>
<script>
export default {
  data() {
    return {
      testArr: [],
      str: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. In, ad numquam laborum quaerat blanditiis tenetur ratione aliquam a nulla. Voluptatem iusto pariatur alias sint dolores quasi quae facilis ipsum maiores?Minima qui incidunt cupiditate molestias assumenda cumque voluptatem! Distinctio vel perspiciatis nisi ad facilis dolor facere sapiente laborum numquam quos? Inventore at vero assumenda, deleniti magnam ab quisquam tempore labore.Aliquid alias perferendis repellendus tempore enim odio nobis vero? Voluptatibus quia quidem, quo explicabo incidunt perferendis debitis cupiditate minus id? Totam provident ducimus expedita possimus veritatis, modi vero obcaecati quae!Sit ea ut nihil maxime, voluptates harum, et at provident laboriosam dolor magnam aspernatur modi earum sint. Ea, voluptates! Pariatur unde dicta at ipsum magnam eligendi id doloribus dolorem reprehenderit.Officia blanditiis minima quasi molestiae odio assumenda suscipit. Corrupti, reiciendis tempore, eaque consequatur fugiat officia ut ab quas voluptatum architecto odit illum beatae optio itaque, rem quos magnam laudantium earum?Natus magni ab asperiores officia impedit laudantium nobis enim unde vero aliquid est, facilis blanditiis esse dolores magnam soluta? Eos dignissimos quas aspernatur sequi vero, facilis harum odio quis commodi.Nam esse quod ducimus, culpa dolor illo quasi inventore error accusantium. Quibusdam laboriosam voluptatem porro, culpa tempora iste officiis deserunt impedit provident quae harum itaque sequi aliquid dignissimos. Fugit, consectetur?Temporibus facilis ut adipisci quia ad dolores dolor unde iste eius sapiente quam modi aliquid qui sint minima cupiditate porro, vel reprehenderit sed expedita dolore dicta, totam eum possimus. Minima!Minima est blanditiis, ratione quam fugiat eaque quo recusandae ullam, repellat, facilis numquam et aspernatur sequi sed expedita in natus perferendis impedit veritatis. Beatae optio perspiciatis, amet ab commodi possimus.Consequuntur, maiores magnam velit nobis doloribus mollitia perferendis possimus fugit porro, totam ad praesentium nihil enim unde est neque nulla eum dicta labore. Animi nostrum doloremque omnis accusamus minima cupiditate!',
    };
  },
  created() {
    for (let i = 0; i < 100000; i++) {
      this.testArr.push({
        key1: this.str,
        key2: this.str,
        key3: this.str,
        key4: this.str,
        key5: this.str,
        key6: this.str,
        key7: this.str,
        key8: this.str,
        key9: this.str,
        key10: this.str,
      });
    }
    console.log('created ... About');
  },
  // beforeUnmount() {
  //   if we add this life cycle then memory will release
  //   this.str = undefined;
  //   this.testArr = undefined;
  // },
  async unmounted() {
    console.log('unmounted About', this.str); //still has value but it should return undefined
  },
};
</script>
