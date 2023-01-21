<script>
export default {
  data() {
    return {
      picked: "One",
      mode: "One",
      nor: "One",
      text: {
        mode:"",
        name:"",
        code:"",
        tel:"",
        select:"",
        nor:"",
        major:"",
        Group:"",
        because:""
      },
    };
  },
};
</script>

<template>
  <div>
    <h1>คําร้องขอลงทะเบียนเกินกว่า หรือ ต่ำกว่าหน่วยกิตที่กําหนด</h1>
    <p>
      ขอลงทะเบียน <input type="radio" id="" value="เกินกว่า" v-model="text.mode" />
      <label for="เกินกว่า">เกินกว่า</label>
      <input type="radio" id="" value="ต่ำกว่า" v-model="text.mode" />
      <label for="ต่ำกว่า">ต่ำกว่า</label>
    </p>
    <div>
      คำนำหน้า <input type="radio" id="o" value="นาย" v-model="picked" />
      <label for="นาย">นาย</label>
      <input type="radio" id="" value="นางสาว" v-model="picked" />
      <label for="นางสาว">นางสาว</label>
      <input type="radio" id="" value="นาง" v-model="picked" />
      <label for="นาง">นาง</label>
      ชื่อ-นามสกุล<input v-model="text.name" placeholder="ชื่อ-นามสกุล" required />
    </div>
    <p>
      รหัสนักศึกษา 10 หลัก:
      <input v-model="text.code" placeholder="รหัสนักศึกษา" required />
    </p>
    <p>เบอร์โทรศัพท์ : 0<input type="tel" v-model="text.tel" placeholder="เบอร์" required /></p>
    <div>
      หลักสูตร :
      <select v-model="text.select">
        <option disabled value=""></option>
        <option>หลักสูตร 4-5 ปี</option>
        <option>หลักสูตร 2 ปีต่อเนื่อง</option>
      </select>
      <input type="radio" id="" value="ปกติ" v-model="text.nor" />
      <label for="ปกติ">ปกติ</label>
      <input type="radio" id="" value="สมทบ" v-model="text.nor" />
      <label for="สมทบ">สมทบ</label>
    </div>
    <div>
      สาขา :
      <select v-model="text.major">
        <option value="เกษตรศาสตร์">เกษตรศาสตร์</option>
        <option value="พืชสวน">พืชสวน</option>
        <option value="เทคโนโลยีอาหาร">เทคโนโลยีอาหาร</option>
        <option value="เทคโนโลยีอุสาหการ การผลิต">เทคโนโลยีอุสาหการ การผลิต</option>
        <option value="เทคโนโลยีพอลิเมอร์">เทคโนโลยีพอลิเมอร์</option>
        <option value="วิศวกรรมเกษตร">วิศวกรรมเกษตร</option>
        <option value="วิศวกรรมอาหาร">วิศวกรรมอาหาร</option>
        <option value="คณิตศาสตร์">คณิตศาสตร์</option>
        <option value="เคมี">เคมี</option>
        <option value="เทคโนโลยีชีวภาพ">เทคโนโลยีชีวภาพ</option>
        <option value="ฟิสิกส์">ฟิสิกส์</option>
        <option value="วัสดุศาสตรฺ">วัสดุศาสตรฺ</option>
        <option value="สถิติ">สถิติ</option>
        <option value="เทคโนโลยีสารสนเทศ">เทคโนโลยีสารสนเทศ</option>
        <option value="วิทยาการคอมพิวเตอร์">วิทยาการคอมพิวเตอร์</option>
        <option value="รัฐประศาสนศาสตร์">รัฐประศาสนศาสตร์</option>
        <option value="รัฐศาสตร์">รัฐศาสตร์</option>
        <option value="การเงิน">การเงิน</option>
        <option value="การจัดการ">การจัดการ</option>
        <option value="การบัญชี">การบัญชี</option>
        <option value="การตลาด">การตลาด</option>
        <option value="ระบบสารสนเทศ">ระบบสารสนเทศ</option>
        <option value="การท่องเที่ยวและการโรงแรม">การท่องเที่ยวและการโรงแรม</option>
        <option value="ประมง">ประมง</option>
        <option value="เศรษฐศาสตร์">เศรษฐศาสตร์</option>
        <option value="นิเทศศาสตร์">นิเทศศาสตร์</option>
        <option value="อังกฤษ">อังกฤษ</option>
        <option value="วิศวกรรมพลังงาน">วิศวกรรมพลังงาน</option>
        <option value="ดิจิทัล">ดิจิทัล</option>
        <option value="ภูมิสถาปัตยกรรม">ภูมิสถาปัตยกรรม</option>
        <option value="วางแผนภาคและเมือง">วางแผนภาคและเมือง</option>
        <option value="สถาปัตยกรรม">สถาปัตยกรรม</option>
        <option value="สัตวศาสตร์">สัตวศาสตร์</option>
        <option value="วนศาสตร์">วนศาสตร์</option>
        <option value="สังคมศาสตร์และพฤติกรรมศาสตร์">สังคมศาสตร์และพฤติกรรมศาสตร์</option>
        <option value="การปกครอง">การปกครอง</option>
      </select>
      คณะ :
      <select name="selectgrop" v-model="text.Group">
        <option value="คณะผลิตกรรมการเกษตร">คณะผลิตกรรมการเกษตร</option>
        <option value="คณะบริหารธุรกิจ">คณะบริหารธุรกิจ</option>
        <option value="คณะวิทยาศาสตร์">คณะวิทยาศาสตร์</option>
        <option value="คณะศิลปศาสตร์">คณะศิลปศาสตร์</option>
        <option value="คณะสถาปัตยกรรมศาสตร์ และการออกแบบสิ่งแวดล้อม ">
          คณะสถาปัตยกรรมศาสตร์ และการออกแบบสิ่งแวดล้อม
        </option>
        <option value="คณะเทคโนโลยีการประมง และทรัพยากรทางน้ำ">
          คณะเทคโนโลยีการประมง และทรัพยากรทางน้ำ
        </option>
        <option value="คณะวิศวกรรมและอุตสาหกรรมเกษตร ">
          คณะวิศวกรรมและอุตสาหกรรมเกษตร
        </option>
        <option value="คณะพัฒนาการท่องเที่ยว ">คณะพัฒนาการท่องเที่ยว</option>
        <option value="คณะเศรษฐศาสตร์ ">คณะเศรษฐศาสตร์</option>
        <option value="วิทยาลัยบริหารศาสตร์ ">วิทยาลัยบริหารศาสตร์</option>
        <option value="วิทยาลัยพลังงานทดแทน ">วิทยาลัยพลังงานทดแทน</option>
        <option value="วิทยาลัยนานาชาติ ">วิทยาลัยนานาชาติ</option>
        <option value="มหาวิทยาลัยแม่โจ้-แพร่ เฉลิมพระเกียรติ ">
          มหาวิทยาลัยแม่โจ้-แพร่ เฉลิมพระเกียรติ
        </option>
        <option value="มหาวิทยาลัยแม่โจ้-ชุมพร ">มหาวิทยาลัยแม่โจ้-ชุมพร</option>
        <option value="คณะพยาบาลศาสตร์">คณะพยาบาลศาสตร์</option>
        <option value="คณะสัตวแพทย์ศาสตร์">คณะสัตวแพทย์ศาสตร์</option>
      </select>
    </div>
    <p>มีความประสงค์จะขอลงทะเบียน</p>
    <div>
      <input type="radio" value="เกินกว่า" v-model="text.mode" />
      <label for="เกินกว่า">เกินกว่า 22 หน่วยกิต</label>
      <br />
      <input type="radio" value="ต่ำกว่า" v-model="text.mode" />
      <label for="ต่ำกว่า">ต่ำกว่า 9 หน่วยกิต</label>
    </div>
    <br />
    <div>
      เนื่องจาก :
      <p style="white-space: pre-line">{{ Text }}</p>
      <textarea
        v-model="text.because"
        placeholder="ข้อความ"
        style="width: 50rem; height: 10rem"
      ></textarea>
    </div>
    <button type="submit">Submit</button>
  </div>
  {{ text }}
</template>

<style scoped></style>
