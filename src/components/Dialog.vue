<template>
  <div class="dialog" title="THÔNG TIN NHÂN VIÊN">
    <div class="form_content_dialog">
        <!--Avatar-->
        <div class="avatar">
            <div class="icon_avatar"></div>
            <span>
                Vui lòng chọn ảnh có định dạng .jpg, .jpeg, .png, .gif
            </span>
        </div>
        <!--Form Input-->
        <form class="form_input">
            <div class="form_left">
                A. THÔNG TIN CHUNG <br />
                <div class="blue_line"></div>
                <label class="input-label">Mã nhân viên (<span style="color: red">*</span>)</label><br />
                <input id="employeeCode" type="text" class="input" onkeyup="NextFocus(event)" placeholder="NV---- (4 chữ số). Ex: NV1234"/>
                <br />
                <label class="input-label">Ngày sinh</label><br />
                <input id="dateOfBirth" type="date" class="input" onkeyup="NextFocus(event)" style="padding-right: 16px" />
                <br />
                <label class="input-label">Số CMTND/ Căn cước (<span style="color: red">*</span>)</label><br />
                <input id="peopleID" type="text" class="input" onkeyup="NextFocus(event)" placeholder="(035)+(9 chữ số) Ex: 035099002083"/>
                <br />
                <label class="input-label">Nơi cấp</label><br />
                <input id="placePeopleID" type="text" class="input" onkeyup="NextFocus(event)" />
                <br />
                <label class="input-label">Email (<span style="color: red">*</span>)</label><br />
                <input id="email" type="email" class="input" onkeyup="NextFocus(event)" placeholder="Ex: example@gmail|yahoo|outlook.com"/>
                <br />
                B. THÔNG TIN CÔNG VIỆC <br />
                <div class="blue_line"></div>
                <label class="input-label">Vị trí</label><br />
                <select id="jobPosition" class="input" onkeyup="NextFocus(event)">
                    <option value="0">Giám đốc</option>
                    <option value="1">Nhân viên Marketing</option>
                    <option value="2">Thủ thư</option>
                    <option value="3">Thư ký</option>
                    <option value="4">Nhân viên</option>
                </select>
                <br />
                <label class="input-label">Mã số thuế cá nhân</label><br />
                <input id="taxCode" type="text" class="input" onkeyup="NextFocus(event)" placeholder="5 kí tự. Ex:1a2b3"/>
                <br />
                <label class="input-label">Ngày gia nhập công ty</label><br />
                <input id="dateStartJob" type="date" class="input" onkeyup="NextFocus(event)" style="padding-right: 16px" />
                <br />
            </div>
            <div class="form_right">
                <label class="input-label">Họ và tên (<span style="color: red">*</span>)</label><br />
                <input id="fullName" type="text" class="input" onkeyup="NextFocus(event)" placeholder="Bắt buộc (4-50) kí tự"/>
                <br />
                <label class="input-label">Giới tính</label><br />
                <select id="gender" class="input" onkeyup="NextFocus(event)">
                    <option value="1">Nam</option>
                    <option value="0">Nữ</option>
                    <option value="2">Khác</option>
                </select>
                <br />
                <label class="input-label">Ngày cấp</label><br />
                <input id="datePeopleID" type="date" class="input" onkeyup="NextFocus(event)" style="padding-right: 16px; margin-bottom: 81px" />
                <br />
                <label class="input-label">Số điện thoại (<span style="color: red">*</span>)</label><br />
                <input id="phoneNumber" type="text" class="input" onkeyup="NextFocus(event)" placeholder="(03)+(8 chữ số)" style="margin-bottom: 44px;"/>
                <br />
                <label class="input-label">Phòng ban</label><br />
                <select id="department" class="input" onkeyup="NextFocus(event)">
                    <option value="0">Phòng nhân sự</option>
                    <option value="1">Phòng Marketing</option>
                    <option value="2">Phòng đào tạo</option>
                    <option value="3">Phòng công nghệ</option>
                </select>
                <br />
                <label class="input-label">Mức lương cơ bản</label><br />
                <input id="salary" type="text" class="input" onkeyup="NextFocus(event)" placeholder="Từ 100.000-999.999.999" />
                <br />
                <label class="input-label">Tình trạng công việc</label><br />
                <select id="jobProperty" class="input" onkeyup="NextFocus(event)">
                    <option value="0">Đang làm việc</option>
                    <option value="1">Đang thử việc</option>
                    <option value="2">Nghỉ việc</option>
                </select>

            </div>
        </form>
    </div>
    <div class="control_dialog">
        <button id="btn_cancel" class="button">Hủy</button>
        <button id="btn_save" class="button"> Lưu</button>
        <button id="btn_update" class="button">Cập nhật</button>
        <button id="btn_delete" class="button">Xóa</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Dialog',
  data() {
    return {

    }
  },
}
</script>

<style>
 /* file dialog.css */
.dialog {
  display: none;

}

  .dialog .form_content_dialog {
      /*background-color: blue;*/
      height: 640px;
      width: 100%;
  }

      .dialog .form_content_dialog .avatar {
          width: 200px;
          height: 100%;
          /*background-color: red;*/
          float: left;
      }


          .dialog .form_content_dialog .avatar .icon_avatar {
              background-image: url('/content/img/default-avatar.jpg');
              width: 150px;
              height: 150px;
              background-size: contain;
              border: 1px solid #d1d1d1;
              border-radius: 50%;
              margin: auto;
          }

          .dialog .form_content_dialog .avatar > span {
              display: inline-block;
              width: 200px;
              text-align: center;
              font-size: 11px;
              margin-top: 5px;
          }

      .dialog .form_content_dialog .form_input input, select {
          width: 90%;
          margin-bottom: 10px;
      }

      .dialog .form_content_dialog .form_left {
          position: absolute;
          width: calc((100% - 200px) / 2);
          height: 600px;
          /*background-color: #ac7148;*/
          left: 200px;
      }

      .dialog .form_content_dialog .form_right {
          position: absolute;
          width: calc((100% - 200px) / 2);
          height: 600px;
          /*background-color: #289a5e;*/
          right: 0;
          padding-top: 34px;
      }
      .dialog .form_content_dialog .input_radio {
  width: 20px;
  height: 20px;
  margin-top: 10px;
  vertical-align: middle;
}
.dialog .control_dialog {
  background-color: #e5e5e5;
  width: 100%;
  height: 60px;
  border-radius: 0 0 5px 5px;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: calc(((100% - 200px) / 2) / 10);
}

  .dialog .control_dialog button {
      margin-left: 10px;
  }

  .dialog .control_dialog #btn_cancel {
      background-color: #e5e5e5;
      color: #000000;
  }

      .dialog .control_dialog #btn_cancel:hover {
          background-color: #BBBBBB;
      }

      .dialog .control_dialog #btn_cancel:active {
          background-color: #E9EBEE;
      }

  .dialog .control_dialog #btn_save {
      background-image: url('/content/icon/icon-save.png');
  }

  .dialog .control_dialog #btn_delete {
      background-color: #F65454;
  }

      .dialog .control_dialog #btn_delete:hover {
          background-color: #c84747;
      }

      .dialog .control_dialog #btn_delete:active {
          background-color: #FF6900;
      }
</style>
