<template>
    <div id="app">
        <toolbar></toolbar>
        <notes-list></notes-list>
        <editor></editor>
    </div>
</template>


<script>
    import Toolbar from './Toolbar.vue'
    import NotesList from './NotesList.vue'
    import Editor from './Editor.vue'

    import {addNote, addFavoriteNode, deleteNote} from '../node_modules/vuex/actions'

    export default{
        vuex: {
            getters: {
                activeNote: state => state.activeNote
            },
            actions: {
                addNote,
                addFavoriteNote,
                deleteNote
            }
        },
        components: {
            Toolbar,
            NotesList,
            Editor
        }
    }
</script>