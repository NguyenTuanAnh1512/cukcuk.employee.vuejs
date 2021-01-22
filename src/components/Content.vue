<template>
  <div class="content">
        <!--Top of Content-->
        <div class="top_of_content_1">
            <p><b>Danh sách nhân viên</b></p>
            <button class="button button-with-icon btn_Add">Thêm nhân viên</button>
        </div>
        <div class="top_of_content_2">
            <div>
                <input id="input_search" class="input input-with-icon input_search" type="text" placeholder="tìm kiếm theo Mã, Tên hoặc Số điện thoại" />
            </div>
            <select class="input select_department">
                <option class="select-option">Tất cả phòng ban</option>
                <option class="select-option">Phòng nhân sự</option>
                <option class="select-option">Phòng đào tạo</option>
                <option class="select-option">Phòng Marketing</option>
                <option class="select-option">Phòng công nghệ</option>
            </select>
            <select class="input select_position">
                <option class="select-option">Tất cả vị trí</option>
                <option class="select-option">Giám đốc</option>
                <option class="select-option">Nhân viên Marketing</option>
                <option class="select-option">Thu ngân</option>
                <option class="select-option">Thư ký</option>
                <option class="select-option">Nhân viên</option>
            </select>

            <button class="btn_refresh">
                <div class="icon_refresh"></div>
            </button>
        </div>

        <!--Table-->
        <div class="table_employee">
            <table id="table_employee">
                <thead>
                  <th style="display: none">EmployeeId</th>
                  <th style="display: none">PeopleID</th>
                  <th style="display: none">DatePeopleID</th>
                  <th style="display: none">PlacePeopleID</th>
                  <th style="display: none">TaxCode</th>
                  <th style="display: none">DateStartJob</th>
                  <th style="width: 7%">Mã nhân viên</th>
                  <th style="width: 13%">Họ và tên</th>
                  <th style="width: 5%">Giới tính</th>
                  <th style="width: 8%">Ngày sinh</th>
                  <th style="width: 10%">Điện thoại</th>
                  <th style="width: 15%">Email</th>
                  <th style="width: 10%">Chức vụ</th>
                  <th style="width: 13%">Phòng ban</th>
                  <th style="width: 10%">Mức lương cơ bản</th>
                  <th style="width: 9%">Tình trạng công việc</th>
                </thead>
                <tbody id="tbody">
                  <Employee />
                  <Employee />
                  <Employee />
                  <Employee />
                </tbody>
            </table>
        </div>

        <!--Paging-->
        <Paging />
    </div>
</template>

<script>
import Paging from './Paging';
import Employee from './Employee';

export default {
  name: 'Content',
  data() {
    return {

    }
  },
  components:{
    Paging,
    Employee,
  }
}
</script>

<style>
  /* file content.css */

.content {
    width: 100%;
    height: calc(100vh - 60px);
    /*padding-left: 16px;*/
}

    .content .top_of_content_1 {
        display: flex;
        align-items: center;
        height: 55px;
        /*background-color: red;*/
    }

        .content .top_of_content_1 p {
            font-size: 20px;
            margin-left: 16px;
        }

        .content .top_of_content_1 .btn_Add {
            position: absolute;
            right: 30px;
            display: flex;
            align-items: center;
            cursor: pointer;
            background-image:url('/content/icon/add.png')
        }

    .content .top_of_content_2 {
        display: flex;
        align-items: center;
        margin-bottom: 20px;
        height: 55px;
        /*background-color: blue;*/
    }

        .content .top_of_content_2 .input {
            margin-right: 20px;
        }

        .content .top_of_content_2 .input_search {
            width: 300px;
            background-image: url('/content/icon/search.png');
            margin-left: 16px;
        }

        .content .top_of_content_2 .select_department{
            width: 170px;
            padding-left: 16px;
            margin-bottom: 0;
        }

        .content .top_of_content_2 .select_position {
            width: 170px;
            padding-left: 16px;
            margin-bottom: 0;
        }

        .content .top_of_content_2 .btn_refresh {
            position: absolute;
            right: 30px;
            background-color: #ffffff;
            border: 1px solid #bbbbbb;
            border-radius: 4px;
            width: 40px;
            height: 40px;
            cursor: pointer;
            outline: none !important;
        }

            .content .top_of_content_2 .btn_refresh:hover {
                background-color: #e9ebee;
            }

            .content .top_of_content_2 .btn_refresh .icon_refresh {
                background-image: url('/content/icon/refresh.png');
                width: 16px;
                height: 16px;
                background-repeat: no-repeat;
                background-size: contain;
                text-align: center;
                margin-left: 5px;
            }



    .content .paging {
        padding-left: 16px;
        padding-right: 30px;
        width: 100%;
        position: absolute;
        bottom: 0px;
        width: 100%;
        height: 56px;
        display: grid;
        grid-template-columns: 200px auto 120px;
        justify-content: space-between;
        align-content: center;
    }

        .content .paging .control_page {
            display: flex;
            align-items: center;
        }

            .content .paging .control_page > div {
                margin-right: 20px;
                cursor: pointer;
            }

            .content .paging .control_page .icon_page {
                width: 26px;
                height: 26px;
                border-radius: 5px;
                background-size: contain;
            }

                .content .paging .control_page .icon_page:hover {
                    background-color: #e3e3e3;
                    border: 1px solid #BBBBBB ;
                }

            .content .paging .control_page .page {
                background-color: #ffffff;
                width: 25px;
                height: 25px;
                border: 1px solid #989898;
                border-radius: 50%;
                text-align: center;
                padding-top: 3px;
            }

                .content .paging .control_page .page:hover {
                    background-color: #e3e3e3;
                }
                .content .table_employee {
    /*background-color: #b6ff00;*/
    width: calc(100% - 16px);
    height: calc(100vh - 60px - 65px - 60px - 56px);
    overflow: auto;
    margin-left: 16px;
    border-bottom: 3px solid #989898;
    padding-right: 16px;
}

    .content .table_employee table {
        border-collapse: collapse;
        width: 100%;
        overflow: auto;

    }

    .content .table_employee th, td {
        padding: 8px;
        text-align: left;
        border-bottom: 1px solid #ddd;
        height: 48px;
    }


    .content .table_employee th {
        position: sticky;
        top: 0;
        width: 100%;
        height: 48px;
        background-color: #bbbbbb;
    }

    .content .table_employee tbody tr:hover {
        background-color: #e3e3e3;
    }
</style>
