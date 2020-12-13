<template>
  <div>
    <!-- Button trigger modal -->
    <button
      type="button"
      class="btn nominate-btn btn-primary"
      data-toggle="modal"
      data-target="#exampleModal"
    >
      Nominate superstar
    </button>

    <!-- Modal -->
    <div
      class="modal fade"
      id="exampleModal"
      tabindex="-1"
      role="dialog"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
            <button
              type="button"
              class="close"
              data-dismiss="modal"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <form>
              <div class="form-group">
                <label for="exampleInputName">Superstar's Name</label>
                <input
                  type="text"
                  class="form-control"
                  id="exampleInputName"
                  placeholder="Enter name"
                  v-model="superstar_name"
                />
              </div>
              <div class="form-group">
                <label for="exampleInputClub">Current Club</label>
                <input
                  type="text"
                  class="form-control"
                  id="exampleInputClub"
                  placeholder="Current club"
                  v-model="current_club"
                />
              </div>
              <div class="form-group">
                <label for="exampleInputNationality">Nationality</label>
                <input
                  type="text"
                  class="form-control"
                  id="exampleInputNationality"
                  placeholder="Nationality"
                  v-model="nationality"
                />
              </div>
              <div class="form-group">
                <label for="exampleInputClubNo">No of Clubs</label>
                <input
                  type="number"
                  min="1"
                  max="20"
                  class="form-control"
                  id="exampleInputClubNo"
                  v-model="no_of_clubs"
                />
              </div>
            </form>
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-dismiss="modal"
            >
              Close
            </button>
            <button
              type="button"
              class="btn btn-primary"
              @click="addNomination"
            >
              Save changes
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      superstar_name: "",
      current_club: "",
      nationality: "",
      no_of_clubs: "",
    };
  },
  methods: {
    addNomination() {
      // insert new nomination into db
      console.log("Add Nomination clicked")
    },
  },
};
</script>
