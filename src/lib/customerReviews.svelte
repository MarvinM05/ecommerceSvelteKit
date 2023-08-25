<script>
  import {reviews} from '../constants'
  import ReviewCard from './reviewCard.svelte'
</script>

<section class='max-container'>
      <h3 class='font-palanquin text-center text-4xl font-bold'>
        What Our
        <span class='text-coral-red'> Customers </span>
        Say?
      </h3>
      <p class='m-auto mt-4 max-w-lg  text-center info-text'>
        Hear genuine stories from our satisfied customers about their
        exceptional experiences with us.
      </p>

      <div class='mt-24 flex flex-1 justify-evenly items-center max-lg:flex-col gap-14'>
        {#each reviews as review}
          <ReviewCard
            key={review.imgURL}
            imgURL={review.imgURL}
            customerName={review.customerName}
            rating={review.rating}
            feedback={review.feedback}
          />
        {/each}
      </div>
    </section>