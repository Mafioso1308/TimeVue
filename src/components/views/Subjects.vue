<template>
  <!-- Main content -->
  <section class="content">
    <!-- Info boxes -->
    <div class="row">

      <div class="col-md-12">
          <div class="box box-info">
            <!-- Input Addons -->

            <div class="box-body text-center">
              <!-- calendar group -->
              <div class="vcenter">
                 <div class="row">
                    <input v-model="subCode"  type="text" placeholder="Enter Subject ID" >

                    <input v-model="division"  type="text" placeholder="division" >

                    <input v-model="tCode" type="text" placeholder="Teacher Code" >
             
                    <button v-on:click="addSubject" class="btn add-button"><i class="fa fa-plus"></i></button>
             
                  </div>
                <!--   <h1>List of Teachers</h1>
                  <table class="table text-center tab">
                    <tr>
                      <th>TeacherId</th>
                      <th>Name</th>
                      <th>Branch</th>
                    </tr>
                    <tr v-for="item in teachers">
                      <td v-text="item.tid"></td>
                      <td v-text="item.tname"></td>
                      <td v-text="item.tbranch"></td>
                    </tr>
                  </table>
                  <router-link to="subjects" class="btn rlink">Assign Subjects</router-link> -->

              <!-- /input-group -->
              </div>
            </div>
            <!-- /.box-body -->
          </div>
        </div>

    </div>
    <!-- /.row -->
  </section>
  <!-- /.content -->
</template>

<script>
  import { mapGetters } from 'vuex'
  export default {
    data: function () {
      return {
        subCode: null,
        division: null,
        tCode: null
      }
    },
    computed: {
      ...mapGetters([
        'isCurrentClassSet'])
    },
    methods: {
      addSubject: function () {
        // TODO code for adding subject here
      }
    }
  }
</script>
