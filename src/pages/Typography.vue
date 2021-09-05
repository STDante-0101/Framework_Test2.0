<template>
  <div class="content">
    <div class="md-layout">
      <div class="md-layout-item md-medium-size-100 md-xsmall-size-100 md-size-100">
        <md-card>
          <md-card-header data-background-color="green">
            <h4 class="title">TO-DOS</h4>
            <p class="category">Aqui temos TO-DOS</p>
          </md-card-header>
          <md-card-content>
            
            <md-table v-model="todos">
                <md-table-row slot="md-table-row" slot-scope="{ item }">
                    <md-table-cell md-label="ID">{{ item.id }}</md-table-cell>
                    <md-table-cell md-label="title">{{ item.title }}</md-table-cell>
                    <md-table-cell md-label="User ID">{{ item.userId }}</md-table-cell>
                </md-table-row>
            </md-table>
    
          </md-card-content>
        </md-card>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
    async mounted(){
        await this.fetchTodos()
    },
    methods: {
        async fetchTodos(){
            const response  = await axios.get('https://jsonplaceholder.typicode.com/todos')
            this.todos = response.data.slice(0, 20)
        }
    },
    data() {
        return {
               todos: [],           
            }
        }
    }
</script>

<style>
.datainfo {
    padding: 10px;
    margin: 10px;
    width: 100%;
    background-color: #d8e0f0;
	display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 1em/2em;
}
</style>


