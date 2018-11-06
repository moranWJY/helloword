# helloword
first 
package A1;
	import java.util.Scanner;
	abstract class Door{
		public static void open(){
			System.out.println("开拍");
		};
		public static void close(){
			System.out.println("关拍");
		}
	}
	interface FireSafe{
		public void fireProof();
	}
	interface BulletSafe{
		public void bulletProof();
	}

	class FireProofDoor extends Door implements FireSafe{
		@Override
		public void fireProof() {
			// TODO Auto-generated method stub
			System.out.println("数码相机"+"25元");
		}
	}
	class BulletProofDoor extends Door implements BulletSafe{

		@Override
		public void bulletProof() {
			// TODO Auto-generated method stub
			System.out.println("单反相机"+"20元");
		}
	}
	class shou extends Door implements FireSafe{
		@Override
		public void fireProof() {
			// TODO Auto-generated method stub
			System.out.println("普通手机"+"10元");
		}
	}
	class zhi extends Door implements BulletSafe{

		@Override
		public void bulletProof() {
			// TODO Auto-generated method stub
			System.out.println("智能手机"+"15元");
		}
	}
	public class A12 {
		public static void main(String[] args) {
			Scanner s = new Scanner(System.in);
			System.out.println("欢迎来到相机拍照店:");
			System.out.println("1.数码相机");
			System.out.println("2.单反相机");
			System.out.println("3.普通手机");
			System.out.println("4.智能手机");
			System.out.println("5.退出");
			System.out.println("请选择业务：");
			String in = s.nextLine();
			FireSafe bus = new FireProofDoor();
			BulletSafe bu = new BulletProofDoor();
			FireSafe ba= new shou();
			BulletSafe pu=new zhi();
			switch (in) {
//				case "1":
//					Door.open();
//				break;
				case "5":
					Door.close();
					System.out.println("谢谢惠顾");
				break;
				case "1":
					bus.fireProof();
					System.out.println("是否开拍？（1.开拍；2.退出）");
					Scanner a1 = new Scanner(System.in);
					int s2 = s.nextInt();
					if(s2==1){
						Door.open();
						System.out.println("已开拍，请付款");
					}
					else{
						System.out.println("请选择其他业务");
						break;
					}
					break;
				case "2":
					bu.bulletProof();
					System.out.println("是否开拍？（1.开拍；2.退出）");
					Scanner a2 = new Scanner(System.in);
					int s3 = s.nextInt();
					if(s3==1){
						Door.open();
						System.out.println("已开拍，请付款");
					}
					else{
						System.out.println("请选择其他业务");
						break;
					}
				break;
				case "3":
					ba.fireProof();
					System.out.println("是否开拍？（1.开拍；2.退出）");
					Scanner a3 = new Scanner(System.in);
					int s4 = s.nextInt();
					if(s4==1){
						Door.open();
						System.out.println("已开拍，请付款");
					}
					else{
						System.out.println("请选择其他业务");
						break;
					}
				break;
				case "4":
					pu.bulletProof();
					System.out.println("是否开拍？（1.开拍；2.退出）");
					Scanner a4 = new Scanner(System.in);
					int s5 = s.nextInt();
					if(s5==1){
						Door.open();
						System.out.println("已开拍，请付款");
					}
					else{
						System.out.println("请选择其他业务");
						break;
					}
					break;
					default:
						System.out.println("其他");
				}
			
		}
		
	}
			
