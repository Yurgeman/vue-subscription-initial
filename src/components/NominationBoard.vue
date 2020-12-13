<template>
    <div>
        <div v-if="loading" class="text-center">
            <img  src="../assets/loading.svg" alt="loader" />
        </div>
        <div v-else>
        <table class="table table-hover">
            <thead class="bg-dark text-white">
            <tr>
                <th scope="col">#</th>
                <th scope="col">Name</th>
                <th scope="col">Current Club</th>
                <th scope="col">No_of_clubs</th>
                <th scope="col">Nationality</th>
            </tr>
            </thead>
            <tbody>
            
            <tr v-for="nomination in nominations" :key="nomination.id">
                <th scope="row">{{ nomination.id }}</th>
                <td>{{ nomination.name }}</td>
                <td>{{ nomination.current_club }}</td>
                <td>{{ nomination.no_of_clubs }}</td>
                <td>{{ nomination.nationality }}</td>
            </tr>
            </tbody>
        </table>

        </div>
    </div>
</template>
<script>

export default {
  data: function() {
    return {
        loading: false,
      nominations: [
        {
          id: 1,
          name: "Ronaldo",
          current_club: "Juventus",
          nationality: "Portugal",
          no_of_clubs: 5
        },
        {
          id: 2,
          name: "Ronaldo",
          current_club: "Juventus",
          nationality: "Portugal",
          no_of_clubs: 5
        },
        {
          id: 3,
          name: "Ibrahimovic",
          current_club: "AC Milan",
          nationality: "Sweden",
          no_of_clubs: 8
        }
      ],
    }
  },
}
</script>