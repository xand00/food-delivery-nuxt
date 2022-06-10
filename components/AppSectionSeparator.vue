<template>
    <div class="section-separator">
      <p class="title"><slot /></p>
      <hr>
    </div>
</template>

<style lang="scss" scoped>
    .section-separator {
        width: 100%;
        display: flex;
        flex-direction: column;
        row-gap: 3rem;
        margin-bottom: 4rem;

        @media (min-width: 64em) {
            max-width: 55.25rem;
            flex-direction: column-reverse;
        }
        
        .title {
            font-weight: 600;
            letter-spacing: 0.00625rem;
            font-size: 1.5rem;
            line-height: 2.25rem;

            @media (min-width: 64em) {
                font-size: 2.75rem;
                line-height: 2.25rem;
            }
        }

        hr {
            height: 0.1875rem;
            background-color: #E4E4E4;
            border: none;
        }
  }
</style>