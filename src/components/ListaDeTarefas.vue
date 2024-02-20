<template>
  <ul class="list-group mt-4">
      <li class="list-group-item" v-for="tarefa in getTarefasFiltradas()">
        <input
          @change="(evento) => (tarefa.finalizada = evento.target.checked)"
          :checked="tarefa.finalizada"
          :id="tarefa.titulo"
          type="checkbox"
          name=""
        />
        <label
          :class="{ done: tarefa.finalizada }"
          class="ms-3"
          :for="tarefa.titulo"
        ></label>
        {{ tarefa.titulo }}
      </li>
    </ul>
</template>