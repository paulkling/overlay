<template>
  <div class="hello" id="page">
    <question>{{ question }}</question>
    <time>{{ time }}</time>
    <helper>{{ helper }}</helper>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    question: String,
    time: String,
    helper: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#page {
  display: grid;
  width: 35%;
  grid-template-areas: "question question time"
                       "helper helper helper"
                       "option text text";
  grid-template-rows: 50px 35px 30px;
  grid-template-columns: 20px 1fr 50px ;
  font: 15px arial;
  background-color: #0a0a0a;
}

#page > time {
  grid-area: time;
  color: #fcfcfc;
  background-color: #42a832;
  text-align: center;
  padding: 15px 0;
 
}

#page > question {
  grid-area: question;
  color: #fcfcfc;
  background-color: #42a832;
  text-align: center;
  padding: 15px 0;
}
#page > helper {
  grid-area: helper;
  color: #fcfcfc;
  background-color: #0a0a0a;
  align-content: center;
  text-align: left;
  padding: 5px 0;
  font-style: italic;
}

#page > option {
  color: #fcfcfc;
  background-color: #787878;
  border: 1px solid #0a0a0a;
  text-align: center;
  padding: 4px 0;
}

#page > text {
  color: #fcfcfc;
  background-color: #787878;
  border: 1px solid #0a0a0a;
  padding: 4px 10px;
  width: 50%

}

#page > vote {
  color: #f3ff12;
  text-align: right;
  padding: 5px 8px;
}


</style>
