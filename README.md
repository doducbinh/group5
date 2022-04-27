# package model;

import java.io.Serializable;
import java.util.Date;
import java.util.Objects;

public class ThiSinh implements Serializable{
	private int maThiSinh;
	private String tenThiSinh;
	private Tinh queQuan;
	private Date ngaySinh;
	private boolean gioiTinh;
	private float diemMon1, diemMon2, diemMon3;
	
	public ThiSinh() {
	}

	public ThiSinh(int maThiSinh, String tenThiSinh, Tinh queQuan, Date ngaySinh, boolean gioiTinh, float diemMon1,
			float diemMon2, float diemMon3) {
		this.maThiSinh = maThiSinh;
		this.tenThiSinh = tenThiSinh;
		this.queQuan = queQuan;
		this.ngaySinh = ngaySinh;
		this.gioiTinh = gioiTinh;
		this.diemMon1 = diemMon1;
		this.diemMon2 = diemMon2;
		this.diemMon3 = diemMon3;
	}

	public int getMaThiSinh() {
		return maThiSinh;
	}

	public void setMaThiSinh(int maThiSinh) {
		this.maThiSinh = maThiSinh;
	}

	public String getTenThiSinh() {
		return tenThiSinh;
	}

	public void setTenThiSinh(String tenThiSinh) {
		this.tenThiSinh = tenThiSinh;
	}

	public Tinh getQueQuan() {
		return queQuan;
	}

	public void setQueQuan(Tinh queQuan) {
		this.queQuan = queQuan;
	}

	public Date getNgaySinh() {
		return ngaySinh;
	}

	public void setNgaySinh(Date ngaySinh) {
		this.ngaySinh = ngaySinh;
	}

	public boolean isGioiTinh() {
		return gioiTinh;
	}

	public void setGioiTinh(boolean gioiTinh) {
		this.gioiTinh = gioiTinh;
	}

	public float getDiemMon1() {
		return diemMon1;
	}

	public void setDiemMon1(float diemMon1) {
		this.diemMon1 = diemMon1;
	}

	public float getDiemMon2() {
		return diemMon2;
	}

	public void setDiemMon2(float diemMon2) {
		this.diemMon2 = diemMon2;
	}

	public float getDiemMon3() {
		return diemMon3;
	}

	public void setDiemMon3(float diemMon3) {
		this.diemMon3 = diemMon3;
	}

	@Override
	public String toString() {
		return "ThiSinh [maThiSinh=" + maThiSinh + ", tenThiSinh=" + tenThiSinh + ", queQuan=" + queQuan + ", ngaySinh="
				+ ngaySinh + ", gioiTinh=" + gioiTinh + ", diemMon1=" + diemMon1 + ", diemMon2=" + diemMon2
				+ ", diemMon3=" + diemMon3 + "]";
	}

	@Override
	public int hashCode() {
		return Objects.hash(diemMon1, diemMon2, diemMon3, gioiTinh, maThiSinh, ngaySinh, queQuan, tenThiSinh);
	}

	@Override
	public boolean equals(Object obj) {
		if (this == obj)
			return true;
		if (obj == null)
			return false;
		if (getClass() != obj.getClass())
			return false;
		ThiSinh other = (ThiSinh) obj;
		return Float.floatToIntBits(diemMon1) == Float.floatToIntBits(other.diemMon1)
				&& Float.floatToIntBits(diemMon2) == Float.floatToIntBits(other.diemMon2)
				&& Float.floatToIntBits(diemMon3) == Float.floatToIntBits(other.diemMon3) && gioiTinh == other.gioiTinh
				&& maThiSinh == other.maThiSinh && Objects.equals(ngaySinh, other.ngaySinh)
				&& Objects.equals(queQuan, other.queQuan) && Objects.equals(tenThiSinh, other.tenThiSinh);
	}
	
}


package model;

import java.io.Serializable;
import java.util.ArrayList;
import java.util.Objects;

public class Tinh implements Serializable{
	private int maTinh;
	private String tenTinh;
	
	public Tinh(int maTinh, String tenTinh) {
		this.maTinh = maTinh;
		this.tenTinh = tenTinh;
	}

	public int getMaTinh() {
		return maTinh;
	}

	public void setMaTinh(int maTinh) {
		this.maTinh = maTinh;
	}

	public String getTenTinh() {
		return tenTinh;
	}

	public void setTenTinh(String tenTinh) {
		this.tenTinh = tenTinh;
	}

	@Override
	public String toString() {
		return "Tinh [maTinh=" + maTinh + ", tenTinh=" + tenTinh + "]";
	}

	@Override
	public int hashCode() {
		return Objects.hash(maTinh, tenTinh);
	}

	@Override
	public boolean equals(Object obj) {
		if (this == obj)
			return true;
		if (obj == null)
			return false;
		if (getClass() != obj.getClass())
			return false;
		Tinh other = (Tinh) obj;
		return maTinh == other.maTinh && Objects.equals(tenTinh, other.tenTinh);
	}
	public static ArrayList<Tinh> getDSTinh(){
		String[] arr_tinh = {"An Giang",
							"Bà Rịa – Vũng Tàu",
							"Bạc Liêu",
							"Bắc Giang",
							"Bắc Kạn",
							"Bắc Ninh",
							"Bến Tre",
							"Bình Dương",
							"Bình Định",
							"Bình Phước",
							"Bình Thuận",
							"Cà Mau",
							"Cao Bằng",
							"Cần Thơ",
							"Đà Nẵng",
							"Đắk Lắk",
							"Đắk Nông",
							"Điện Biên",
							"Đồng Nai",
							"Đồng Tháp",
							"Gia Lai",
							"Hà Giang",
							"Hà Nam",
							"Hà Nội",
							"Hà Tĩnh",
							"Hải Dương",
							"Hải Phòng",
							"Hậu Giang",
							"Hòa Bình",
							"Thành phố Hồ Chí Minh",
							"Hưng Yên",
							"Khánh Hòa",
							"Kiên Giang",
							"Kon Tum",
							"Lai Châu",
							"Lạng Sơn",
							"Lào Cai",
							"Lâm Đồng",
							"Long An",
							"Nam Định",
							"Nghệ An",
							"Ninh Bình",
							"Ninh Thuận",
							"Phú Thọ",
							"Phú Yên",
							"Quảng Bình",
							"Quảng Nam",
							"Quảng Ngãi",
							"Quảng Ninh",
							"Quảng Trị",
							"Sóc Trăng",
							"Sơn La",
							"Tây Ninh",
							"Thái Bình",
							"Thái Nguyên",
							"Thanh Hóa",
							"Thừa Thiên Huế",
							"Tiền Giang",
							"Trà Vinh",
							"Tuyên Quang",
							"Vĩnh Long",
							"Vĩnh Phúc",
							"Yên Bái"};
		

		ArrayList<Tinh> listTinh = new ArrayList<Tinh>();
		int i = 0;
		for (String tenTinh : arr_tinh) {
			Tinh t = new Tinh(i, tenTinh);
			listTinh.add(t);
		}
		return listTinh;
	}

	public static Tinh getTinhById(int queQuan) {
		return Tinh.getDSTinh().get(queQuan);
	}

	public static Tinh getTinhByTen(String tenTinh) {
		ArrayList<Tinh> listTinh = Tinh.getDSTinh();
		for (Tinh tinh : listTinh) {
			if(tinh.tenTinh.equals(tenTinh))
				return tinh;
		}
		return null;
	}
}
