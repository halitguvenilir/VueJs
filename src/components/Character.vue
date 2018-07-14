<template>
    <div class="col-xs-12 col-md-6 character">
        <div class="character-button">
            <button class="btn btn-success" @click="switchCharacter">Change Character</button>
        </div>
        <div class="card">
            <h3 class="card-title"><strong>Character Name:</strong> {{ character.name }}</h3>
            <p class="card-text"><strong>Character Height:</strong> {{ character.height }}</p>
            <p class="card-text"><strong>Character Mass:</strong> {{ character.mass }}</p>
            <p class="card-text"><strong>Character Hair Color:</strong> {{ character.hair_color }}</p>
            <p class="card-text"><strong>Character Skin Color:</strong> {{ character.skin_color }}</p>
            <p class="card-text"><strong>Character Eye Color:</strong> {{ character.eye_color }}</p>
            <p class="card-text"><strong>Character Birth Year:</strong> {{ character.birth_year }}</p>
            <p class="card-text"><strong>Character Gender:</strong> {{ character.gender }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['id'],
        data() {
            return {
                character: {}
            }
        },
        methods: {
            fetchCharacter(id) {
                fetch(`https://swapi.co/api/people/${id}`, {
                    method: 'GET'
                })
                .then(response => response.json())
                .then(json => this.character = json)
            },
            switchCharacter() {
                let random_id = Math.floor(Math.random() * 83) + 1
                this.fetchCharacter(random_id)
            }
        },
        created() {
            this.fetchCharacter(this.id)
        }
    }
</script>

<style>
strong {
    color: #f0ad4e;
}

.character {
    margin-bottom: 30px;
}

.character-button {
    padding-bottom: 30px;
}

.card {
    border: 2px solid #4fc08d;
    border-radius: 5px;
    padding: 5px;
}
</style>