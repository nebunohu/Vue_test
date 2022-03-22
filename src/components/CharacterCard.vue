<template>
    <article class="cardWrapper" @click={clickHandler}>
      <img class="cardImage" src="charactersList[0].image" alt='' />
      <div class="infoWrapper">
        <ul>
          <li class="characterName">{{charactersList[0].name}}</li>
          <li class="characterStatus"> /> {{charactersList[0].status}} - {{charactersList[0].species}}</li>
          <li>Last known location: {{charactersList[0].location.name}}</li>
        </ul>
      </div>
    </article>
</template>

<script>

export default {
  name: "CharacterCard",
  setup() {
    

  },
  props: {
    charactersList: Array
  },
  beforeMount() {
    /*const CharacterCard = ({character}) => {
    const dispatch = useDispatch();
    const clickHandler = (event) => {
      dispatch(setIsModalOpened());
      dispatch(setCurrentCharacter(character));
    }*/
  },
  methods: {
    clickHandler: function() {

    }
  }
}
</script>
