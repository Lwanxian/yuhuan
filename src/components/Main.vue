<template>
  <div class="background" style="width: 100vw; height: 100vh">
    <!-- 系统标题栏 -->
    <div class="nav">
      <div class="title">宇环数控信息化智能系统</div>
      <div class="titleen">Yuhuan CNC information intelligent system</div>
    </div>
    <!-- 内容栏 -->
    <div class="con">
      <!-- 第一列 -->
      <div class="col1">
        <div class="con-pronum">
          <div class="con-pronum-title">生产数据统计</div>
          <!-- 数据表格 -->
          <div class="con-pronum-table">
            <el-table
              :data="tableData"
              style="width: 100%"
              height="600"
              :cell-style="rowStyle"
              :header-cell-style="tableHeaderColor"
              :default-sort="{ prop: 'date', order: 'descending' }"
              stripe="true"
            >
              <el-table-column
                prop="machineid"
                label="机台号"
                width="70"
                align="center"
              ></el-table-column>
              <el-table-column
                prop="plannum"
                sortable
                label="计划加工件数"
                width="120"
                align="center"
              ></el-table-column>
              <el-table-column
                prop="realnum"
                sortable
                label="实际加工件数"
                align="center"
              >
              </el-table-column>
              <el-table-column
                prop="endvalue"
                sortable
                label="完成率"
                align="center"
              >
              </el-table-column>
            </el-table>
          </div>
        </div>
        <div class="con-warn"></div>
      </div>
      <!-- 第二列 -->
      <div class="col2"></div>
      <!-- 第三列 -->
      <div class="col3">
        <div class="con-trace"></div>
        <div class="con-health"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tableData: [
        {
          machineid: "#25",
          plannum: "1600",
          realnum: " 1518",
          endvalue: "90%",
        },
        {
          machineid: "#00",
          plannum: "1598",
          realnum: " 1518",
          endvalue: "90%",
        },
        {
          machineid: "#31",
          plannum: "1655",
          realnum: " 1582",
          endvalue: "92%",
        },
        {
          machineid: "#25",
          plannum: "1600",
          realnum: " 1518",
          endvalue: "90%",
        },
        {
          machineid: "#00",
          plannum: "1598",
          realnum: " 1518",
          endvalue: "90%",
        },
        {
          machineid: "#31",
          plannum: "1655",
          realnum: " 1582",
          endvalue: "92%",
        },
        {
          machineid: "#25",
          plannum: "1600",
          realnum: " 1518",
          endvalue: "90%",
        },
        {
          machineid: "#00",
          plannum: "1598",
          realnum: " 1518",
          endvalue: "90%",
        },
        {
          machineid: "#31",
          plannum: "1655",
          realnum: " 1582",
          endvalue: "92%",
        },
        {
          machineid: "#25",
          plannum: "1600",
          realnum: " 1518",
          endvalue: "90%",
        },
        {
          machineid: "#00",
          plannum: "1598",
          realnum: " 1518",
          endvalue: "90%",
        },
        {
          machineid: "#31",
          plannum: "1655",
          realnum: " 1582",
          endvalue: "92%",
        },
      ],
    };
  },
  methods: {
    formatter(row, column) {
      return row.plannum;
    },
    rowStyle({ row, rowIndex }) {
      if ((row)) {
        return {
          color: "rgb(102,198,220,1)",
          backgroundColor: "rgb(14,17,41,.75)",
          fontSize: "10px",
        };
      }
    },
    //设置表格头的样式
    tableHeaderColor({ row, column, rowIndex, columnIndex }) {
      return "background-color:#0E1129;color:#fff;font-size:10px;text-align:center";
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.background {
  background-image: url("../assets/beijing.jpg");
  background-size: cover;
}
.nav {
  width: 99%;
  height: 60px;
}
.title {
  color: aliceblue;
  text-align: center;
  line-height: 40px;
  font-family: "pangmenzhengdao";
  font-size: 30px;
}
.titleen {
  color: rgb(86, 182, 244);
  text-align: center;
  font-size: 10px;
}
.con {
  margin-top: 10px;
  width: 99%;
  height: 990px;
  display: flex;
  justify-content: space-between;
}
.col1 {
  width: 490px;
  height: 990px;
}
.con-pronum {
  position: relative;
  width: 490px;
  height: 670px;
  background-color: rgb(14, 17, 41, 0.7);
  border: rgb(89, 89, 89) 1px solid;
}
.con-pronum-title {
  width: 180px;
  height: 40px;
  line-height: 50px;
  text-align: center;
  margin: auto;
  color: aliceblue;
  font-family: "pangmenzhengdao";
  letter-spacing: 2px;
  border-top: transparent;
  border-bottom: rgb(255, 255, 244) 1px solid;
  border-radius: 30%;
}
.con-warn {
  margin-top: 8px;
  width: 490px;
  height: 308px;
  background-color: rgb(14, 17, 41, 0.7);
  border: rgb(89, 89, 89) 1px solid;
}
.col2 {
  margin-top: 15px;
  width: 904px;
  height: 973px;
  background-color: rgb(14, 17, 41, 0.7);
  border: rgb(89, 89, 89) 1px solid;
}
.col3 {
  width: 490px;
  height: 990px;
}
.con-trace {
  width: 490px;
  height: 478px;
  background-color: rgb(14, 17, 41, 0.7);
  border: rgb(89, 89, 89) 1px solid;
}
.con-health {
  margin-top: 8px;
  width: 490px;
  height: 500px;
  background-color: rgb(14, 17, 41, 0.7);
  border: rgb(89, 89, 89) 1px solid;
}
.con-pronum-table {
  width: 100%;
  height: 600px;
  bottom: 0;
  position: absolute;
}
/* 设置滚动条的宽度 */
</style>
