<script>
export default{
  data: () => ({
    searchQuery:'',

      todos: [
        { name: "Project A", users: 4, dashboards: 3, category: "D"},
        { name: "Project B", users: 2, dashboards: 4, category: "C"},
        { name: "Project C", users: 1, dashboards: 2, category: "F"},
        { name: "Project D", users: 3, dashboards: 2, category: "D"},
      ],
      sstt:[
        "textA",
        "textB",
        "textC",
        "textD",
      ],
    circle:[
      "ProjectCircleA",
      "ProjectCircleB",
      "ProjectCircleC",
      "ProjectCircleD",
    ],
    projectbox:[
      "ProjectboxA",
      "ProjectboxB",
      "ProjectboxC",
      "ProjectboxD",
    ],
    deletebox:[
      "delteA",
      "delteB",
      "delteC",
      "delteD",
    ],
    userbox:[
      "userA",
      "userB",
      "userC",
      "userD",
    ],
    minidashboardBox:[
      "dashboardA",
      "dashboardB",
      "dashboardC",
      "dashboardD",
    ],
    projectname:[
      "projectA",
      "projectB",
      "projectC",
      "projectD",
    ],
    dashboardtext:[
      "dashboardtextA",
      "dashboardtextB",
      "dashboardtextC",
      "dashboardtextD",
    ]

  }),
  methods: {
    removeTodo(todo) {
    this.todos.splice(this.todos.indexOf(todo),1);
    // this.todos = this.todos.filter( (t) => t !==todo)
    },

    filterItems: function(todos){
      var app = this;
      return todos.filter(function(todos) {
        let regex = new RegExp('(' + app.searchQuery + ')', 'i');
        return todos.name.match(regex);
      })
    }
  }
}

</script>

<template>
    <!-- delete button   -->
    <div :class = "deletebox[index]" v-for="(todo,index) in todos">
      <button @click="removeTodo(todo)" class= "removeTodo">Delete</button>
    </div>
    <div id="app">
    
    <input v-model="searchQuery" class="searchbox" placeholder="Search for a keyword" />
 
    <div v-for = "(todo,index) in filterItems(todos)" :key="todos.name">
    <div :class = "sstt[index]"  >{{todo.category}}</div>
    <div :class = "userbox[index]"    >{{todo.users+" users"}}</div>
    <div :class = "projectname[index]" >{{todo.name}}</div>
    <div :class = "dashboardtext[index]"  >{{todo.dashboards+ " dashboards"}}</div>
     </div>
      </div>
       
     
  

  <ProjectboxA>
    <div class="leftbox">
      
    </div>

  </ProjectboxA>

  <ProjectboxB>
    <div class="leftbox">
      
    </div>

  </ProjectboxB>

  <ProjectboxC>
    <div class="leftbox">
      
    </div>
    
  </ProjectboxC>

  <ProjectboxD>
    <div class="leftbox">
      
    </div>
    
  </ProjectboxD>
  
  <ProjectCircleA>

  </ProjectCircleA>

  <ProjectCircleB>

  </ProjectCircleB>

  <ProjectCircleC>

  </ProjectCircleC>

  <ProjectCircleD>

  </ProjectCircleD>

 <dashboardA></dashboardA>
<dashboardB></dashboardB>
<dashboardC></dashboardC>
<dashboardD></dashboardD>

  
</template>

<style >

@media ( min-width: 10px) {




  ProjectboxA{
    position: absolute;
    background: #FFFFFF;
    box-shadow: 0px 4px 20px rgba(120, 120, 120, 0.15);
    border-radius: 8px;
    position: absolute;
    width: 1145px;
    height: 70px;
    left: 135.62px;
    top: 260px;
  }

  ProjectboxA .leftbox{
    width: 10.5px;
    height: 70px;
    left: 135.62px;
    top: 260px;
    /* Green */

    background: #00CC74;
    border-radius: 4px 0px 0px 4px;
  }
  
  ProjectboxB{
    position: absolute;
    background: #FFFFFF;
    box-shadow: 0px 4px 20px rgba(120, 120, 120, 0.15);
    border-radius: 8px;
    position: absolute;
    width: 1145px;
    height: 70px;
    left: 135.62px;
    top: 338px;
  }
  ProjectboxB .leftbox{
    width: 10.5px;
    height: 70px;
    left: 135.62px;
    top: 338px;

    /* Purple */

    background: #B37FEB;
    border-radius: 4px 0px 0px 4px;

  }

  ProjectboxC{
    position: absolute;
    background: #FFFFFF;
    box-shadow: 0px 4px 20px rgba(120, 120, 120, 0.15);
    border-radius: 8px;
    position: absolute;
    width: 1145px;
    height: 70px;
    left: 135.62px;
    top: 416px;
  }

  ProjectboxC .leftbox{
    width: 10.5px;
    height: 70px;
    left: 135.62px;
    top: 416px;

    /* Bright Blue */

    background: #1990FF;
    border-radius: 4px 0px 0px 4px;
  }

  ProjectboxD{
    position: absolute;
    background: #FFFFFF;
    box-shadow: 0px 4px 20px rgba(120, 120, 120, 0.15);
    border-radius: 8px;
    position: absolute;
    width: 1145px;
    height: 70px;
    left: 135.62px;
    top: 494px;
  }

  ProjectboxD .leftbox{
    width: 10.5px;
    height: 70px;
    left: 135.62px;
    top: 494px;

    /* Green */

    background: #00CC74;
    border-radius: 4px 0px 0px 4px;
  }

  ProjectCircleA {
    position: absolute;
    width: 28px;
    height: 28px;
    left: 161px;
    top: 281px;
    border-radius: 50%;

    /* GreenOpacity */

    background: #CCF5E3;
  }

  ProjectCircleB {
    position: absolute;
    width: 28px;
    height: 28px;
    left: 161px;
    top: 359px;
    border-radius: 50%;

    /* PurpleOpacity */

    background: #F0E5FB;
  }

  ProjectCircleC {
    position: absolute;
    width: 28px;
    height: 28px;
    left: 161px;
    top: 437px;
    border-radius: 50%;

    /* BrightBlueOpacity */

    background: #D1E9FF;
  }

  ProjectCircleD {
    position: absolute;
    width: 28px;
    height: 28px;
    left: 162px;
    top: 515px;
    border-radius: 50%;

    /* GreenOpacity */

    background: #CCF5E3;
  }
.textA{
    position: absolute;
    width: 26px;
    height: 16px;
    left: 162px;
    top: 284px;
 		z-index:1;

    /* Header 3 */

    font-family: 'Roboto Medium';
    font-size: 14px;
    line-height: 22px;
    /* or 157% */

    text-align: center;

    /* Green */

    color: #00CC74;
  }

  .textB{
    position: absolute;
    width: 26px;
    height: 16px;
    left: 162px;
    top: 362px;
    z-index:1;

    /* Header 3 */

    font-family: 'Roboto Medium';
    font-size: 14px;
    line-height: 22px;
    /* or 157% */

    text-align: center;

    /* Purple */

    color: #B37FEB;
  }
  .textC{
    position: absolute;
    width: 26px;
    height: 16px;
    left: 162px;
    top: 440px;
    z-index:1;

    /* Header 3 */

    font-family: 'Roboto Medium';
    font-size: 14px;
    line-height: 22px;
    /* or 157% */

    text-align: center;

    /* Bright Blue */

    color: #1990FF;
  }
  .textD{
    position: absolute;
    width: 26px;
    height: 16px;
    left: 163px;
    top: 518px;
    z-index:1;

    /* Header 3 */

    font-family: 'Roboto Medium';
    font-size: 14px;
    line-height: 22px;
    /* or 157% */

    text-align: center;

    /* Green */

    color: #00CC74;

  }
  .delteA{
    position: absolute;
    width: 161.51px;
    height: 22px;
    left: 1206px;
    top: 284px;
    z-index:1;

    /* Paragraph Regular */

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    /* identical to box height, or 157% */


    /* Red */

    color: #DD1155;
  }
  .delteB{
    position: absolute;
    width: 161.51px;
    height: 22px;
    left: 1208px;
    top: 361px;
    z-index:1;

    /* Paragraph Regular */

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    /* identical to box height, or 157% */


    /* Red */

    color: #DD1155;

  }
  .delteC{
    position: absolute;
    width: 161.51px;
    height: 22px;
    left: 1208px;
    top: 439px;
    z-index:1;

    /* Paragraph Regular */

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    /* identical to box height, or 157% */


    /* Red */

    color: #DD1155;
  }
  .delteD{
    position: absolute;
    width: 161.51px;
    height: 22px;
    left: 1208px;
    top: 515px;
    z-index:1;

    /* Paragraph Regular */

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    /* identical to box height, or 157% */


    /* Red */

    color: #DD1155;
    
  }
  .userA{
    position: absolute;
    width: 161.51px;
    height: 22px;
    left: 753px;
    top: 288px;
    z-index:1;

    /* Paragraph Regular */

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    /* identical to box height, or 157% */


    /* Dark Grey */

    color: #52594D;
      }
  
    .userB{
    position: absolute;
    width: 161.51px;
    height: 22px;
    left: 753px;
    top: 362px;
    z-index:1;

    /* Paragraph Regular */

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    /* identical to box height, or 157% */


    /* Dark Grey */

    color: #52594D;
      }
  .userC{
    position: absolute;
    width: 161.51px;
    height: 22px;
    left: 753px;
    top: 440px;
    z-index:1;

    /* Paragraph Regular */

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    /* identical to box height, or 157% */
    /* Dark Grey */

    color: #52594D;
  }
  .userD{
    position: absolute;
    width: 161.51px;
    height: 22px;
    left: 753px;
    top: 518px;
    z-index:1;

    /* Paragraph Regular */

    font-family: 'Roboto';
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    /* identical to box height, or 157% */


    /* Dark Grey */

    color: #52594D;
  }
  dashboardA{
    box-sizing: border-box;

/* Auto layout */

    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 4px 16px;
    gap: 10px;


    position: absolute;
    width: 117px;
    height: 22px;
    left: 991px;
    top: 284px;

    /* GreenOpacity */

    background: #CCF5E3;
    /* Green */

    border: 1px solid #00CC74;
    border-radius: 4px;
      }

    dashboardB{
      box-sizing: border-box;

    /* Auto layout */

    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 4px 16px;
    gap: 10px;
    z-index:1;

    position: absolute;
    width: 117px;
    height: 22px;
    left: 991px;
    top: 360px;

    /* GreenOpacity */

    background: #CCF5E3;
    /* Green */

    border: 1px solid #00CC74;
    border-radius: 4px;
    }
    
    dashboardC{
      box-sizing: border-box;

      /* Auto layout */

      display: flex;
      flex-direction: row;
      align-items: center;
      padding: 4px 16px;
      gap: 10px;
      z-index:1;

      position: absolute;
      width: 119px;
      height: 22px;
      left: 989px;
      top: 438px;

      /* GreenOpacity */

      background: #CCF5E3;
      /* Green */

      border: 1px solid #00CC74;
      border-radius: 4px;
    }

    dashboardD{
      box-sizing: border-box;

      /* Auto layout */

      display: flex;
      flex-direction: row;
      align-items: center;
      padding: 4px 16px;
      gap: 10px;
      z-index:1;

      position: absolute;
      width: 117px;
      height: 22px;
      left: 989px;
      top: 516px;

      /* GreenOpacity */

      background: #CCF5E3;
      /* Green */

      border: 1px solid #00CC74;
      border-radius: 4px;
    }

    .projectA{
      position: absolute;
      width: 232.41px;
      height: 22px;
      left: 226.22px;
      top: 284px;
      z-index:1;

      /* Header 3 */

      font-family: 'Roboto Medium';
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 22px;
      /* identical to box height, or 157% */


      /* Dark Blue */

      color: #223273;
    }

    .projectB{
      position: absolute;
      width: 232.41px;
      height: 22px;
      left: 226.22px;
      top: 362px;
      z-index:1;

      /* Header 3 */

      font-family: 'Roboto Medium';
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 22px;
      /* identical to box height, or 157% */


      /* Dark Blue */

      color: #223273;
    }

    .projectC{
      position: absolute;
      width: 232.41px;
      height: 22px;
      left: 226.22px;
      top: 440px;
      z-index:1;

      /* Header 3 */

      font-family: 'Roboto Medium';
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 22px;
      /* identical to box height, or 157% */


      /* Dark Blue */

      color: #223273;
    }

    .projectD{
      position: absolute;
      width: 232.41px;
      height: 22px;
      left: 226.22px;
      top: 518px;
      z-index:1;
      /* Header 3 */

      font-family: 'Roboto Medium';
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 22px;
      /* identical to box height, or 157% */


      /* Dark Blue */

      color: #223273;
    }

    .dashboardtextA{
      position: absolute;
      width: 117px;
      height: 22px;
      left: 1002px;
      top: 284px;
      z-index:2;


      /* Button Regular */

      font-family: 'Roboto';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 14px;
      /* identical to box height, or 100% */

      display: flex;
      align-items: center;
      text-align: center;

      /* Green */

      color: #00CC74;
      flex: none;
      order: 0;
      flex-grow: 0;
    }
    
    .dashboardtextB{
      
      position: absolute;
      width: 117px;
      height: 22px;
      left: 1002px;
      top: 360px;
      z-index:2;

      /* Button Regular */

      font-family: 'Roboto';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 14px;
      /* identical to box height, or 100% */

      display: flex;
      align-items: center;
      text-align: center;

      /* Green */

      color: #00CC74;


      /* Inside auto layout */

      flex: none;
      order: 0;
      flex-grow: 0;
          }

    .dashboardtextC{
      
      position: absolute;
      width: 119px;
      height: 22px;
      left: 1002px;
      top: 438px;
      z-index:2;

      /* Button Regular */

      font-family: 'Roboto';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 14px;
      /* identical to box height, or 100% */

      display: flex;
      align-items: center;
      text-align: center;

      /* Green */

      color: #00CC74;


      /* Inside auto layout */

      flex: none;
      order: 0;
      flex-grow: 0;
    }

    .dashboardtextD{
      
      position: absolute;
      width: 117px;
      height: 22px;
      left: 1002px;
      top: 516px;
      z-index:2;

      /* Button Regular */

      font-family: 'Roboto';
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 14px;
      /* identical to box height, or 100% */

      display: flex;
      align-items: center;
      text-align: center;

      /* Green */

      color: #00CC74;


      /* Inside auto layout */

      flex: none;
      order: 0;
      flex-grow: 0;
    }
    
    searchbox{
      
    box-sizing: border-box;
    z-index:2;
    position: absolute;
      width: 220px;
      height: 40px;
      left: 1002px;
      top: 516px;

    background: #FFFFFF;
    /* Grey */

    border: 1px solid #C4C4C4;
    border-radius: 8px;

    }
}
</style>
