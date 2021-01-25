<template>
<div>
    <table>
        <thead>
            <th>ID</th>
            <th>Name</th>
            <th>Intro</th>
        </thead>
        <tbody>
            <!-- <tr>
                <td>1</td>
                <td>travel_club1</td>
                <td>welcome our club1</td>
            </tr> -->
            <tr v-for="(travelClub,index) in travelClubs" :key="index">
                <td>{{travelClub.id}}</td>
                <td>{{travelClub.name}}</td>
                <td>{{travelClub.intro}}</td>
            </tr>
        </tbody>
    </table>
    <ol>
        <li v-for="(value, name, index) in travelClub" :key="index">
            index:{{index}}, name : {{name}}, value : {{value}}
        </li>
    </ol>
</div>
</template>

<script>
const travelClubs = [
    {
        id:"1",
        name:"travel_club1",
        intro:"welcome our 1 club"
    },
    {
        id:"2",
        name:"travel_club2",
        intro:"welcome our 2 club"
    },
    {
        id:"3",
        name:"travel_club3",
        intro:"welcome our 3 club"
    }
]
const travelClub = {id : "4", name:"travel club 4", intro : "welcome our 4 club"}
export default {
    name:"ForDirective",
    data: function(){
        return {
            travelClubs: travelClubs,
            travelClub: travelClub
        }
    },
}
</script>

<style>

</style>