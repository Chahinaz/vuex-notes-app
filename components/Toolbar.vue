<template>
    <div id="toolbar">
        <i @click="addNote" class="glyphicon-plus"></i>
        <i @click="addFavoriteNote" class="glyphicon glyphicon-star"
            :class="{starred: activeNote.favorite}"></i>
        <i @click="deleteNote" class="glyphicon glyphicon-remove"></i>
    </div>
</template>

<script>
    import {addNote, addFavoriteNote, deleteNote} from '../node_modules/vuex/actions'

    export default {
        vuex: {
            getters: {
                activeNote: state => state.activeNote
            },
            actions: {
                addNote,
                addFavoriteNote,
                deleteNote
            }
        }
    }

</script>