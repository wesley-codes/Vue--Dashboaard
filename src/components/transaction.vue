<template>
    <div class="transaction">
        <div class="person">
            <img src="https://res.cloudinary.com/drh4lw1m7/image/upload/v1683640343/IMG_0747_jmrmd5.jpg"  alt="person" class="avatar">
            <div class="person-info">
                <h2 class="person-name">{{ person.name }}</h2>
                <h4 class="person-nick">Lima</h4>
            </div>
        </div>
        <div class="transaction-info">
            <h2 class="transaction-info-heading">{{ projects }}</h2>
            <h4 class="transaction-info-text">Projects</h4>
        </div>
        <div class="transaction-info">
            <h2 class="transaction-info-heading">{{ finished }}</h2>
            <h4 class="transaction-info-text">Finished Projects</h4>
        </div>
        <div class="transaction-info">
            <h2 class="transaction-info-heading purple">$ {{ profit }}</h2>
            <h4 class="transaction-info-text">Total Profit</h4>
        </div>
        <div class="transaction-info">
            <h2 class="transaction-info-heading">{{ followers }}</h2>
            <h4 class="transaction-info-text">Followers</h4>
        </div>
        <img class="arrow" src="../assets/icons/Right.svg" alt="arrow">
    </div>
</template>

<script>

export default {
  name: 'transaction',
  props: [
    'person',
    'projects',
    'finished',
    'profit',
    'followers'
  ],
  
}

</script>

<style scoped>
    .transaction {
        grid-column: span 9;
        justify-content: space-between;
        align-items: center;
        background-color: white;
        padding: 1rem;
        display: grid;
        grid-template-columns: 1.5fr 1fr 1fr 1fr 1fr 0.2fr;
        cursor: pointer;
        animation: fadeIn .2s ease-out;
        transition: background-color .2s;
    }

    .transaction:hover {
        background-color: #F8F8F8;
    }
    .avatar{
width: 100px;
height: 100px;
border-radius: 50px;
    }

    .person {
        display: flex;
        align-items: center;
        grid-column: 1;
    }

    .person-info {
        margin: 0 0 0 1.5rem;
    }

    .transaction-info-text {
        color: rgba(0, 0, 0, .4);
    }

    .person-nick {
        color: rgba(0, 0, 0, .4);
    }

    .purple {
        color: var(--purple);
    }

    @keyframes fadeIn {
        0% { transform: scale(0) }
        100% { transform: scale(1) }
    }

    @keyframes hover {
        0% { transform: rotate(0deg) ;}
        100% { transform: rotate(360deg) ;}
    }
</style>
