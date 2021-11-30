# Báo cáo về 23 mẫu thiết kế

***Nhóm chúng em gồm các thành viên:***

*- Nguyễn Anh Đức 20021336*

*- Nguyễn Thị Thúy Quỳnh 20021426*

*- Đặng Thành Trung 20021455*

Trong quá trình tìm kiếm, phân tích, nhóm em đã tìm được một số repo mã nguồn trên github có 23 mẫu thiết kế như sau.

## Tóm tắt:
*Nhóm em đã tìm và phân tích 4 repo:*

	 1. https://github.com/shuleisanshi/myblog
	 
	 2. https://github.com/simple-android-framework/android_design_patterns_analysis
	 
	 3. https://github.com/braisdom/ObjectiveSql
	 
	 4. https://github.com/Anuken/Mindustry
	 
	 *Trong đó, repo 2 là code minh họa 23 design patterns, các repo còn lại là các dự án thực tế.*

## Repo 1: Link https://github.com/shuleisanshi/myblog

- *Giới thiệu:* Repo này là mã nguồn của 1 blog cá nhân của tác giả. 
Trong repo này, tác giả đã sử dụng 1 mẫu thiết kế thuộc nhóm *Structural* là **Adapter**.

* Dễ thấy, mẫu thiết kế **Adapter** được tác giả áp dụng 10 lần, theo từng nhóm các lớp và giao diện, mỗi nhóm đều có đầy đủ Adaptee, Adapter, Target và Client:
  + Các Adaptee là các giao diện không tương thích, cần được tích hợp, nằm trong package [mapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper), gồm: [ArticleMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/ArticleMapper.java), [CategoryMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/CategoryMapper.java), [CommentMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/CommentMapper.java), [LinkMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/LinkMapper.java), [MenuMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/MenuMapper.java), [NoticeMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/NoticeMapper.java), [OptionMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/OptionMapper.java), [PageMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/PageMapper.java), [TagMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/TagMapper.java), [UserMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/UserMapper.java).
  + Các Target một interface chứa các chức năng được sử dụng bởi Client, nằm trong package [service](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service), gồm : [ArticleService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/ArticleService.java), [CategoryService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/CategoryService.java), [CommentService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/CommentService.java), [LinkService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/LinkService.java), [MenuService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/MenuService.java), [NoticeService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/NoticeService.java), [OptionService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/OptionService.java), [PageService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/PageService.java), [TagService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/TagService.java), [UserService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/UserService.java).
  + Các Adapter (lớp tích hợp, giúp interface không tương thích tích hợp được với interface đang làm việc, thực hiện việc chuyển đổi và kết nối Adaptee với Client) tương ứng với các Adaptee trên nằm trong package [impl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl) lần lượt là:  [ArticleServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/ArticleService.java), [CategoryServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/CategoryService.java), [CommentServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/CommentService.java), [LinkServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/LinkService.java), [MenuServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/MenuService.java), [NoticeServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/NoticeService.java), [OptionServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/CategoryService.java), [PageServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/CategoryService.java), [TagServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/CategoryService.java), [UserServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/CategoryService.java).
  + Các Client là các lớp sử dụng các đối tượng có interface Target thuộc package [controller](https://github.com/shuleisanshi/myblog/tree/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/controller) (bao gồm 2 package bên trong là: [admin](https://github.com/shuleisanshi/myblog/tree/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/controller/admin) và [home](https://github.com/shuleisanshi/myblog/tree/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/controller/admin)).

  + Ta có thể quan sát rõ hơn qua ví dụ về các lớp và giao diện liên quan tới menu:
	- Giao diện [MenuMapper](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/mapper/MenuMapper.java):
	```java
	public interface MenuMapper {

	    int deleteById(Integer menuId);

	    int insert(Menu menu);

	    Menu getMenuById(Integer menuId);
	    
	    int update(Menu menu);

	    List<Menu> listMenu() ;
	}
	```
		Giao diện trên có chứa các phương thức dùng để chèn, xóa, cập nhật menu và một phương thức trả về 1 menu với mã số cho trước.

	- Giao diện [MenuService](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/MenuService.java) (vai trò Target):
	```java
	public interface MenuService {
	
	    List<Menu> listMenu();

	    Menu insertMenu(Menu menu);

	    void deleteMenu(Integer id);

	    void updateMenu(Menu menu);

	    Menu getMenuById(Integer id);
	}
	```
		Giao diện này có chứa các phương thức dùng để chèn, xóa, cập nhật menu và một phương thức trả về 1 menu với mã số cho trước gần như giống hệt với adaptee MenuMapper, chỉ khác tên và khác kiểu trả về của phương thức update(Menu);
	
	- Lớp [MenuServiceImpl](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/service/impl/MenuService.java) (vai trò Adapter):
	```java
	public class MenuServiceImpl implements MenuService {

	    @Autowired(required = false)
	    private MenuMapper menuMapper;

	    @Override
	    public List<Menu> listMenu() {
		List<Menu> menuList = menuMapper.listMenu();
		return menuList;
	    }

	    @Override
	    public Menu insertMenu(Menu menu) {
		menuMapper.insert(menu);
		return menu;
	    }

	    @Override
	    public void deleteMenu(Integer id) {
		menuMapper.deleteById(id);
	    }

	    @Override
	    public void updateMenu(Menu menu) {
		menuMapper.update(menu);
	    }

	    @Override
	    public Menu getMenuById(Integer id) {
		return menuMapper.getMenuById(id);
	    }
	}
	```
		Lớp này cài đặt tất cả các phương thức trong giao diện MenuService (target).
	
	- Lớp [BackMenuController](https://github.com/shuleisanshi/myblog/blob/f337b7bded4bdc343227a467873e5cfdafac39c4/src/main/java/com/shulei/ssm/blog/controller/admin/BackMenuController.java) (vai trò Client):
	```java
	@Controller
	@RequestMapping("/admin/menu")
	public class BackMenuController {

	    @Autowired
	    private MenuService menuService;

	    @RequestMapping(value = "")
	    public String menuList(Model model)  {
		List<Menu> menuList = menuService.listMenu();
		model.addAttribute("menuList",menuList);
		return "admin/menu/index";
	    }

	    @RequestMapping(value = "/insertSubmit",method = RequestMethod.POST)
	    public String insertMenuSubmit(Menu menu)  {
		if(menu.getMenuOrder() == null) {
		    menu.setMenuOrder(1);
		}
		menuService.insertMenu(menu);
		return "redirect:/admin/menu";
	    }

	    @RequestMapping(value = "/delete/{id}")
	    public String deleteMenu(@PathVariable("id") Integer id)  {
		menuService.deleteMenu(id);
		return "redirect:/admin/menu";
	    }

	    @RequestMapping(value = "/edit/{id}")
	    public ModelAndView editMenuView(@PathVariable("id") Integer id)  {
		ModelAndView modelAndView = new ModelAndView();

		Menu menu =  menuService.getMenuById(id);
		modelAndView.addObject("menu",menu);

		List<Menu> menuList = menuService.listMenu();
		modelAndView.addObject("menuList",menuList);

		modelAndView.setViewName("admin/menu/edit");
		return modelAndView;
	    }

	    @RequestMapping(value = "/editSubmit",method = RequestMethod.POST)
	    public String editMenuSubmit(Menu menu)  {
		menuService.updateMenu(menu);
		return "redirect:/admin/menu";
	    }
	}
	```
		Đây là lớp dùng để điều khiến, quản lý menu dành riêng cho admin. Lớp này có chứa 1 thuộc tính kiểu MenuService.
	
   + **Nhận xét:** Khi đối chiếu với mẫu thiết kế Adapter chuẩn trên trang [GPCoder](https://gpcoder.com/4483-huong-dan-java-design-pattern-adapter/), em nhận thấy mẫu thiết kế tác giả dùng ở đây là hoàn toàn tương đồng với mô hình ***Object Adapter – Composition (Chứa trong)*** được nhắc trong bài viết (có lớp mới (Adapter) tham chiếu đến một đối tượng của lớp có sẵn với interface không tương thích (Adaptee), đồng thời cài đặt interface mà người dùng mong muốn (Target), khác với *Class Adapter – Inheritance (Kế thừa)* là mô hình mà lớp mới (Adapter) kế thừa lớp có sẵn với interface không tương thích (Adaptee)).

	Điểm khác biệt nhỏ ở đây là trong repo *my_blog* này, mẫu thiết kế Adapter được áp dụng trên quy mô rộng hơn (tới 10 lần) và ở trong môi trường phức tạp hơn so với trên GPCoder.


### Repo 2: Link https://github.com/simple-android-framework/android_design_patterns_analysis

Đây là 1 repo tóm tắt (bằng tiếng Trung Quốc) về tất cả 23 mẫu thiết kế cơ bản. Trong đó, có 9 mẫu thiết kế có mã nguồn trong repo.

Các mẫu được chia theo 3 nhóm mẫu thiết kế:

#### Creational Design Patterns:

	*Repo có 2 mẫu thiết kế thuộc nhóm *Creational* là *Builder* và *Prototype*.

* [**Builder**](https://github.com/simple-android-framework/android_design_patterns_analysis/tree/master/builder/mr.simple):
  Tác giả đưa ra ví dụ về mẫu thiết kế Builder trong file [readme.md](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/builder/mr.simple/readme.md) của mục này. Ví dụ về việc dùng mẫu thiết kế Builder để tạo các đối tượng máy tính (Computer):
	```java
	public abstract class Computer {
		protected int mCpuCore = 1;
		protected int mRamSize = 0;
		protected String mOs = "Dos";

		protected Computer() {
		}

		public abstract void setCPU(int core);

		public abstract void setRAM(int gb);

		public abstract void setOs(String os);

		@Override
		public String toString() {
			return "Computer [mCpuCore=" + mCpuCore + ", mRamSize=" + mRamSize
					+ ", mOs=" + mOs + "]";
		}
	}

	public class AppleComputer extends Computer {

		protected AppleComputer() {
		}

		@Override
		public void setCPU(int core) {
			mCpuCore = core;
		}

		@Override
		public void setRAM(int gb) {
			mRamSize = gb;
		}

		@Override
		public void setOs(String os) {
			mOs = os;
		}
	}

	public abstract class Builder {
	
		public abstract void buildCPU(int core);

		public abstract void buildRAM(int gb);

		public abstract void buildOs(String os);

		public abstract Computer create();
	}

	public class ApplePCBuilder extends Builder {
		private Computer mApplePc = new AppleComputer();

		@Override
		public void buildCPU(int core) {
			mApplePc.setCPU(core);
		}

		@Override
		public void buildRAM(int gb) {
			mApplePc.setRAM(gb);
		}

		@Override
		public void buildOs(String os) {
			mApplePc.setOs(os);
		}

		@Override
		public Computer create() {
			return mApplePc;
		}
	}

	public class Director {
		Builder mBuilder = null;

		public Director(Builder builder) {
			mBuilder = builder;
		}

		public void construct(int cpu, int ram, String os) {
			mBuilder.buildCPU(cpu);
			mBuilder.buildRAM(ram);
			mBuilder.buildOs(os);
		}
	}

	public class Test {
		public static void main(String[] args) {
			Builder builder = new ApplePCBuilder();
			Director pcDirector = new Director(builder);
			pcDirector.construct(4, 2, "Mac OS X 10.9.1");
			System.out.println("Computer Info : " + builder.create().toString());
		}
	}
	```
  + **Nhận xét:** Mẫu thiết kế này có đầy đủ các thành phần chuẩn như mẫu trên [GPCoder](https://gpcoder.com/4434-huong-dan-java-design-pattern-builder/):
	- Builder: là lớp trừu tượng *Builder*, khai báo phương thức tạo đối tượng Computer chung.
	- ConcreteBuilder: là lớp *ApplePCBuilder*, khai báo phương thức tạo đối tượng Computer.
	- Product : là lớp *AppleComputer* (kế thừa lớp trừu tượng *Computer*), đại diện cho đối tượng cần tạo, đối tượng này phức tạp, có nhiều thuộc tính.
	- Director: là lớp *Director*, là nơi gọi tới Builder để tạo ra đối tượng.
	
	Điểm khác biệt giữa 2 mẫu thiết kế là thành phần *Builder* của repo này là lớp trừu tượng, còn thành phần Builder ở trang GPCoder là một giao diện.
	
* [**Prototype**](https://github.com/simple-android-framework/android_design_patterns_analysis/tree/master/prototype/mr.simple):
    + Phần code tìm được trong repo gồm lớp *WordDocument* (implements *Cloneable*) đóng vai trò ConcretePrototype: lớp này thực thi interface được cung cấp bởi Prototype để copy (nhân bản) chính bản thân nó. Các lớp này chính là thể hiện cụ thể phương thức clone().
	
      Ở đây, *Cloneable* là Prototype.
	```java
	public class WordDocument implements Cloneable {
	    private String mText;
	    private ArrayList<String><string> mImages = new ArrayList<String><string>();

	    public WordDocument() {
		System.out.println("----------- WordDocument构造函数 -----------");
	    }

	    @Override
	    protected WordDocument clone() {
		try {
		    WordDocument doc = (WordDocument) super.clone();
		    doc.mText = this.mText;
		    doc.mImages = this.mImages;
		    return doc;
		} catch (Exception e) {
		}

		return null;
	    }

	    public String getText() {
		return mText;
	    }

	    public void setText(String mText) {
		this.mText = mText;
	    }

	    public List<string> getImages() {
		return mImages;
	    }

	    public void addImage(String img) {
		this.mImages.add(img);
	    }

	    public void showDocument() {
		System.out.println("----------- Word Content Start -----------");
		System.out.println("Text : " + mText);
		System.out.println("Images List: ");
		for (String imgName : mImages) {
		    System.out.println("image name : " + imgName);
		}
		System.out.println("----------- Word Content End -----------");
	    }
	}
	```
    + Class Client được dùng để tạo mới object bằng cách gọi Prototype thực hiện clone chính nó.
	```java
	public class Client {
	    public static void main(String[] args) {
		WordDocument originDoc = new WordDocument();
		originDoc.setText("这是一篇文档");
		originDoc.addImage("图片1");
		originDoc.addImage("图片2");
		originDoc.addImage("图片3");
		originDoc.showDocument();

		WordDocument doc2 = originDoc.clone();
		doc2.showDocument();

		doc2.setText("这是修改过的Doc2文本");
		doc2.showDocument();

		originDoc.showDocument();
	    }
	}
	```
    + **Nhận xét:** Mẫu thiết kế được dùng trong repo hoàn toàn giống với mẫu chuẩn tại [GPCoder](https://gpcoder.com/4413-huong-dan-java-design-pattern-prototype/).

#### Nhóm Structural Design Patterns:

	*Repo có 3 mẫu thiết kế thuộc nhóm *Structural* là *Bridge*, *Composite* và *Facade*.

* [**Bridge**](https://github.com/simple-android-framework/android_design_patterns_analysis/tree/master/bridge/shen0834):

	Đây là 1 đoạn code liên quan đến việc xử lý với các hình cơ bản như hình chữ nhật, hình tròn.
	```java
	public class DP1 {
		...
	}
	
	public class DP2 {
		...
	}
	
	abstract class Shape {
		protected Drawing myDrawing;

		public Shape(Drawing drawing) {
			this.myDrawing = drawing;
		}

		abstract public void draw();

		protected void drawRectangle(){
	       //this.impl.implmentation()
			myDrawing.drawRantangle();
		}

		protected void drawCircle(){
		//this.impl.implmentation()
			myDrawing.drawCircle();
		}
	}
	
	public class Rantangle extends Shape{
		public Rantangle(Drawing drawing) {
			super(drawing);
		}

		@Override
		public void draw() {
			drawRectangle();
		}
	}
	
	public class Circle extends Shape {
		public Circle(Drawing drawing) {
			super(drawing);
		}
		@Override
		public void draw() {
			drawCircle();
		}
	}
	
	public interface Drawing {
		public void drawRantangle();
		public void drawCircle();
	}
	
	public class V1Drawing implements Drawing {

		DP1 dp1;

		public V1Drawing() {
			dp1 = new DP1();
		}
		@Override
		public void drawRantangle() {
			dp1.draw_1_Rantanle();
		}
		@Override
		public void drawCircle() {
			dp1.draw_1_Circle();
		}			
	}
	
	public class V2Drawing implements Drawing {
		DP2 dp2;

		public V2Drawing() {
			dp2 = new DP2();
		}

		@Override
		public void drawRantangle() {
			dp2.drawRantanle();
		}
		@Override
		public void drawCircle() {
			dp2.drawCircle();
		}
	}
	```
   + **Nhận xét:**  Khi đối chiếu đoạn code trên với mẫu thiết kế chuẩn trên [GPCoder](https://gpcoder.com/4520-huong-dan-java-design-pattern-bridge/), em thấy 2 mẫu hoàn toàn trùng khớp, không có thay đổi gì. Cụ thể hơn, trong tình huống này, dễ dàng nhận thấy lớp *Shape* đóng vai trò *Abstraction*, các lớp *Circle* và *Rantangle* là các *Refined Abstraction*, giao diện *Drawing* đóng vai trò *Implementor* với 2 *ConcreteImplementor* là V1Drawing và V2Drawing.
	
* [**Composite**](https://github.com/simple-android-framework/android_design_patterns_analysis/tree/master/composite/tiny-times):
	
	Tác giả đưa ra ví dụ về mẫu thiết kế Builder trong file [readme.md](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/composite/tiny-times/readme.md) của mục này. Mẫu thiết kế được đưa ra ở đây giống hệt mẫu chuẩn trên [GPCoder](https://gpcoder.com/4554-huong-dan-java-design-pattern-composite/).
	
* [**Facade**](https://github.com/simple-android-framework/android_design_patterns_analysis/tree/master/facade/elsdnwn):
    + Tác giả đưa ra ví dụ minh họa về mẫu thiết kế được dùng trong quản lý một chiếc ti vi, với các lớp và giao diện:
	- Lớp TvController đóng vai trò Facade: biết rõ lớp của hệ thống con nào đảm nhận việc đáp ứng yêu cầu của client, sẽ chuyển yêu cầu của client đến các đối tượng của hệ thống con tương ứng: 
		```java
		public class TvController {
		    private PowerSystem mPowerSystem = new PowerSystem();
		    private VoiceSystem mVoiceSystem = new VoiceSystem();
		    private ChannelSystem mChannelSystem = new ChannelSystem();

		    public void powerOn() {
			mPowerSystem.powerOn();
		    }

		    public void powerOff() {
			mPowerSystem.powerOff();
		    }

		    public void turnUp() {
			mVoiceSystem.turnUp();
		    }

		    public void turnDown() {
			mVoiceSystem.turnDown();
		    }

		    public void nextChannel() {
			mChannelSystem.next();
		    }

		    public void prevChannel() {
			mChannelSystem.prev();
		    }
		}
		```
	- Lớp PowerSystem, VoiceSystem, ChannelSystem đóng vai trò Subsystems: cài đặt các chức năng của hệ thống con, xử lý công việc được gọi bởi Facade. Các lớp này không cần biết Facade và không tham chiếu đến nó.
		```java
		 class PowerSystem {
		    public void powerOn() {
			System.out.println("开机");
		    }

		    public void powerOff() {
			System.out.println("关机");
		    }
		}
		
		class VoiceSystem {
		    public void turnUp() {
			System.out.println("音量增大");
		    }

		    public void turnDown() {
			System.out.println("音量减小");
		    }
		}
		
		class ChannelSystem {
		    public void next() {
			System.out.println("下一频道");
		    }

		    public void prev() {
			System.out.println("上一频道");
		    }
		}
		```
    + **Nhận xét:** Phần này của repo đã thể hiện một cách trực quan và thực tế về mẫu thiết kế *Facade*.
	 
	  Tuy nhiên, trong ví dụ minh họa có một hạn chế là không chỉ rõ Client (đối tượng sử dụng Facade để tương tác với các subsystem) nên chưa thực sự đầy đủ nếu so với code mẫu trên [GPCoder](https://gpcoder.com/4604-huong-dan-java-design-pattern-facade/).
	
#### Nhóm Behaviorial Design Patterns:

	*Repo có 4 mẫu thiết kế thuộc nhóm *Behaviorial* là *Command*, *Iterator*, *Factory Method* và **.
	
* [**Command**](https://github.com/simple-android-framework/android_design_patterns_analysis/tree/master/command/lijunhuayc/resource/command):
    Trong package [*command*](https://github.com/simple-android-framework/android_design_patterns_analysis/tree/master/command/lijunhuayc/resource/command), có các lớp và giao diện dùng để làm việc với các đối tượng [PeopleBean](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/command/lijunhuayc/resource/command/PeopleBean.java) (chứa các thông tin của một người), gồm:
	+ Giao diện [Command](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/command/lijunhuayc/resource/command/Command.java):
	```java
	public interface Command {
		public void execute();
		public void undo();
		public void redo();

	}
	```
		Giao diện này thể hiện đúng vai trò của thành phần Command trong mẫu thiết kế Command.
	+ Lớp [ConcreteCommandImpl1](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/command/lijunhuayc/resource/command/ConcreteCommandImpl1.java) (ngoài ra còn các lớp với vai trò tương đương trong cấu trúc chương trình là [ConcreteCommandImpl2](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/command/lijunhuayc/resource/command/ConcreteCommandImpl2.java) và [ConcreteCommandImpl3](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/command/lijunhuayc/resource/command/ConcreteCommandImpl.java)):
	```java
	public class ConcreteCommandImpl1 implements Command{
		private ReceiverRole receiverRole1;

		public ConcreteCommandImpl1(ReceiverRole receiverRole1) {
			this.receiverRole1 = receiverRole1;
		}

		@Override
		public void execute() {
			receiverRole1.opActionUpdateAge(1001);
		}

		@Override
		public void undo() {
			receiverRole1.rollBackAge();
		}

		@Override
		public void redo() {
		}
	    }
	```
		 Các lớp này thể hiện đúng vai trò của thành phần ConcreteCommand trong mẫu thiết kế Command.
	+ Lớp [ReceiverRole](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/command/lijunhuayc/resource/command/ReceiverRole.java):
	```java
	public class ReceiverRole {
		private PeopleBean people; 
		private PeopleBean peopleCache = new PeopleBean();     	

	      public ReceiverRole() {
		this.people = new PeopleBean(-1, "NULL");
	      }

	      public ReceiverRole(PeopleBean people) {
		this.people = people;
	      }

	      public void opActionUpdateAge(int age) {
		System.out.println("执行命令前："+people.toString());
		this.people.update(age);
		System.out.println("执行命令后："+people.toString()+"\n");
	      }

	      public void opActionUpdateName(String name) {
		System.out.println("执行命令前："+people.toString());
		this.people.update(name);
		System.out.println("执行命令后："+people.toString()+"\n");
	      }

	      public void rollBackAge() {
		people.setAge(peopleCache.getAge());
		System.out.println("命令回滚后："+people.toString()+"\n");
	      }
	      public void rollBackName() {
		people.setName(peopleCache.getName());
		System.out.println("命令回滚后："+people.toString()+"\n");
	      }
	}
	```
		Lớp này thể hiện đúng vai trò của thành phần Receiver trong mẫu thiết kế Command.
	+ Lớp [ClientRole](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/command/lijunhuayc/resource/command/ClientRole.java):
	```java
	public class ClientRole {
	    public void assembleAction() {
			ReceiverRole receiverRole1 = new ReceiverRole();
			Command command1 = new ConcreteCommandImpl1(receiverRole1);           		    
		Command command2 = new ConcreteCommandImpl2(receiverRole1);

			InvokerRole invokerRole = new InvokerRole();
			invokerRole.setCommand1(command1);
			invokerRole.setCommand2(command2);
			invokerRole.invoke(0);			
			invokerRole.invoke(1);				
	    }
	}
	```
		Lớp này thể hiện đúng vai trò của thành phần Client trong mẫu thiết kế Command.
	+ Lớp [InvokerRole](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/command/lijunhuayc/resource/command/Invoker.java):
	```java
	public class InvokerRole {
	    private Command command1;
	    private Command command2;

	    public void setCommand1(Command command1) {
			this.command1 = command1;
	    }
	    public void setCommand2(Command command2) {
			this.command2 = command2;
	    }

	    public void invoke(int args) {
			if(args == 0){
				command1.execute();
				command2.execute();
			} else if(args == 1){
				command1.undo();
				command2.undo();
			}
	    }   	
	}
	```
		Lớp này thể hiện đúng vai trò của thành phần Invoker trong mẫu thiết kế Command.
		
  + **Nhận xét:**  Khi đối chiếu đoạn code trên với mẫu thiết kế chuẩn trên [GPCoder](https://gpcoder.com/4686-huong-dan-java-design-pattern-command/), em thấy 2 mẫu hoàn toàn trùng khớp, không có thay đổi gì, thể hiện qua các lớp và giao diện: Command, ConcreteCommandImpl1, ConcreteCommandImpl2, ConcreteCommandImpl3, ClientRole, InvokerRole, ReceiverRole như trên.

* [**Iterator**](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/iterator/haoxiqiang):
  Tác giả đưa ra ví dụ về mẫu thiết kế Iterator trong file [AndroidMileage.java](https://github.com/simple-android-framework/android_design_patterns_analysis/blob/master/iterator/haoxiqiang/resource/AndroidMileage.java): 
	```java
	public class AndroidMileage {

	    final static int[] versionCodes;
	    final static String[] versionMileages;
	    final static int size;

	    static {
		versionCodes = new int[]{ /**some code*/ ... };
		versionMileages = new String[]{ /**some code*/ ... };

		size =  Math.min(versionCodes.length, versionMileages.length);
	    }

	    public static class Mileage implements NameValuePair {

		public String name;
		public String value;

		@Override
		public String getName() {
		    return name;
		}

		@Override
		public String getValue() {
		    return value;
		}

		@Override
		public String toString() {
		    return "versionCode:" + name + " desc:" + value;
		}
	    }


	    public Iterator<Mileage> iterator() {
		return new ArrayIterator();
	    }

	    private class ArrayIterator implements Iterator<Mileage> {
		/**
		 * Number of elements remaining in this iteration
		 */
		private int remaining = size;

		/**
		 * Index of element that remove() would remove, or -1 if no such elt
		 */
		private int removalIndex = -1;

		@Override
		public boolean hasNext() {
		    return remaining != 0;
		}

		@Override
		public Mileage next() {
		    Mileage mileage = new Mileage();
		    removalIndex = size-remaining;
		    mileage.name = String.valueOf(versionCodes[removalIndex]);
		    mileage.value = versionMileages[removalIndex];
		    remaining-=1;
		    return mileage;
		}

		@Override
		public void remove() {
		    versionCodes[removalIndex]=-1;
		    versionMileages[removalIndex]="It was set null";
		}
	    }
	}
	```
  + **Nhận xét:**  Khi đối chiếu đoạn code trên với mẫu thiết kế chuẩn trên [GPCoder](https://gpcoder.com/4724-huong-dan-java-design-pattern-iterator/), em thấy mẫu thiết kế trong repo này có điểm tương đồng với mẫu chuẩn ở chỗ có đầy đủ các thành phân: 
	- Aggregate (interface NameValuePair) là một interface định nghĩa định nghĩa các phương thức để tạo Iterator object.
	- ConcreteAggregate (class Mileage) cài đặt các phương thức của Aggregate, nó cài đặt interface tạo Iterator để trả về một thể hiện của ConcreteIterator thích hợp.
	- Iterator (class Iterator<Mileage> - tổng quát là Iterator<T>) là một interface hay abstract class, định nghĩa các phương thức để truy cập và duyệt qua các phần tử.
	- ConcreteIterator (class ArrayIterator) cài đặt các phương thức của Iterator, giữ index khi duyệt qua các phần tử.
	- Client (class AndroidMileage) đối tượng sử dụng Iterator Pattern, nó yêu cầu một iterator từ một đối tượng collection để duyệt qua các phần tử mà nó giữ. Các phương thức của iterator được sử dụng để truy xuất các phần tử từ collection theo một trình tự thích hợp.
    + Điểm khác biệt của project này là ở chỗ tất cả các lớp và giao diện đêu là inner class (lớp trong) của Client (class AndroidMileage).
	
* [**Factory Method**](https://github.com/simple-android-framework/android_design_patterns_analysis/tree/master/factory-method/AigeStudio): 
     **Nhận xét:** Mẫu thiết kế được dùng trong repo hoàn toàn giống với mẫu chuẩn tại [GPCoder](https://gpcoder.com/4413-huong-dan-java-design-pattern-prototype/).
	
* [**Strategy**]():
    + Repo minh họa về các hàm dùng để tính các phép toán cơ bản (+, -, *, /) với 2 số thục:
	- Giao diện *Strategy* : định nghĩa các hành vi có thể có của một Strategy.
		```java
		public interface Strategy {
			public double calc(double paramA, double paramB);
		}
		```
	- Các lớp *AddStrategy, SubStrategy, MultiStrategy, DivStrategy* đóng vai trò ConcreteStrategy: cài đặt các hành vi cụ thể của Strategy.
		```java
		public class AddStrategy implements Strategy {
			@Override
			public double calc(double paramA, double paramB) {
				System.out.println("执行加法策略...");
				return paramA + paramB;
			}
		}

		public class SubStrategy implements Strategy {
			@Override
			public double calc(double paramA, double paramB) {
				System.out.println("执行减法策略...");
				return paramA - paramB;
			}
		}

		public class MultiStrategy implements Strategy {
			@Override
			public double calc(double paramA, double paramB) {
				System.out.println("执行乘法策略...");
				return paramA * paramB;
			}
		}

		public class DivStrategy implements Strategy {
			@Override
			public double calc(double paramA, double paramB) {
				System.out.println("执行除法策略...");
				if (paramB == 0) {
					throw new IllegalArgumentException("除数不能为0!");
				}
				return paramA / paramB;
			}
		}
		```
	- Lớp *Calc* đóng vai trò Context: chứa một tham chiếu đến đối tượng Strategy và nhận các yêu cầu từ Client, các yêu cầu này sau đó được ủy quyền cho Strategy thực hiện.
		```java
		public class Calc {
			private Strategy strategy;
			public void setStrategy(Strategy strategy) {
				this.strategy = strategy;
			}

			public double calc(double paramA, double paramB) {
				if (this.strategy == null) {
					throw new IllegalStateException("你还没有设置计算的策略");
				}
				return this.strategy.calc(paramA, paramB);
			}
		}
		```
    + **Nhận xét:** Mẫu thiết kế được dùng trong repo hoàn toàn giống với mẫu chuẩn tại [GPCoder](https://gpcoder.com/4796-huong-dan-java-design-pattern-strategy/).
	
	
## Repo 3: Link https://github.com/braisdom/ObjectiveSql

Dựa vào mẫu thiết kế Active record khuyến khích phát triển nhanh chóng và làm sạch, mã có ít nhất và quy ước về cấu hình.

Interface ORMFramework trong package benchmark.
```java
public interface ORMFramework {

    void initialize() throws Exception;

    void update() throws Exception;

    User query() throws Exception;

    void teardown();

    class Factory {

        public static ORMFramework createORMFramework(String frameworkName, HikariDataSource dataSource) {
            switch (frameworkName) {
                case MyBatis.FRAMEWORK_NAME:
                    return new MyBatis(dataSource);
                case Jdbc.FRAMEWORK_NAME:
                    return new Jdbc(dataSource);
                case ObjectiveSQL.FRAMEWORK_NAME:
                    return new ObjectiveSQL(dataSource);
                case Hibernate.FRAMEWORK_NAME:
                    return new Hibernate(dataSource);
                default:
                    throw new IllegalArgumentException("Cannot find ORM framework: " + frameworkName);
            }
        }
    }
}
```

Lớp User trong package benchmark.
```java
public class User implements Serializable {

    @Id
    @PrimaryKey
    private Integer id;
    private String name;
    private int age;

    @Transient
    @javax.persistence.Transient
    private Map<String, Object> rawAttributes = new HashMap<>();

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public Map<String, Object> getRawAttributes() {
        return rawAttributes;
    }
}
```
Lớp ObjectiveSQL trong package benchmark.
```java
public class ObjectiveSQL implements ORMFramework, ConnectionFactory, Logger, LoggerFactory {

    public static final String FRAMEWORK_NAME = "objsql";

    private final HikariDataSource dataSource;

    public ObjectiveSQL(HikariDataSource dataSource) {
        this.dataSource = dataSource;

        Databases.installConnectionFactory(this);
        Databases.installLoggerFactory(this);
    }

    @Override
    public void initialize() throws Exception {
        Databases.execute("insert into user(id, name, age) values(1, 'ash', 25)");
    }

    @Override
    public void update() throws Exception {
        User.update("age = 12", "id = ?", 1);
    }

    @Override
    public User query() throws Exception {
        return User.queryByPrimaryKey(1);
    }

    @Override
    public void teardown() {
        dataSource.close();
    }

    @Override
    public Connection getConnection(String dataSourceName) throws SQLException {
        return dataSource.getConnection();
    }

    @Override
    public void debug(long elapsedTime, String sql, Object[] params) {
        // Do nothing
    }

    @Override
    public void info(long elapsedTime, String sql, Object[] params) {
        // Do nothing
    }

    @Override
    public void error(String message, Throwable throwable) {
        // Do nothing
    }

    @Override
    public Logger create(Class<?> clazz) {
        return new ObjectiveSQL(dataSource);
    }
}
```

Lớp Hibernate trong package benchmark.
```java
public class Hibernate implements ORMFramework {

    public static final String FRAMEWORK_NAME = "hibernate";

    private final HikariDataSource dataSource;
    private final SessionFactory sessionFactory;

    public Hibernate(HikariDataSource dataSource) {
        this.dataSource = dataSource;
        sessionFactory = new Configuration()
                .configure()
                .buildSessionFactory();
    }

    @Override
    public void initialize() throws Exception {
        Session session = sessionFactory.openSession();
        session.beginTransaction();
        User user = new User();
        user.setId(1);
        user.setName("ash");
        user.setAge(25);
        session.save( user );
        session.getTransaction().commit();
        session.close();
    }

    @Override
    public void update() {
        Session session = sessionFactory.openSession();
        session.beginTransaction();
        User user = new User();
        user.setId(1);
        user.setName("ash");
        user.setAge(15);
        session.update(user);
        session.getTransaction().commit();
        session.close();
    }

    @Override
    public User query() throws Exception {
        Session session = sessionFactory.openSession();
        Query<User> query = session.createQuery("from com.github.braisdom.objsql.benchmark.User " +
                "user where user.id = 1");
        User user = query.getSingleResult();
        session.close();
        return user;
    }

    @Override
    public void teardown() {
        dataSource.close();
        sessionFactory.close();
    }
}
```

## Repo 4: Link https://github.com/Anuken/Mindustry

Sử dụng mẫu thiết kế:

Strategy với:

Interface: SlotAssignmentStrategy

```java
public interface SlotAssignmentStrategy{

    /** Updates the assignment of members to slots */
    void updateSlotAssignments(Seq<SlotAssignment> assignments);

    /** Calculates the number of slots from the assignment data. */
    int calculateNumberOfSlots(Seq<SlotAssignment> assignments);

    /** Removes the slot assignment at the specified index. */
    void removeSlotAssignment(Seq<SlotAssignment> assignments, int index);

}
```
Các ConcreteStategy: BoundedSlotAssignmentStrategy, DistanceAssignmentStrategy, FreeSlotAssignmentStrategy

```java
public abstract class BoundedSlotAssignmentStrategy implements SlotAssignmentStrategy{

    @Override
    public abstract void updateSlotAssignments(Seq<SlotAssignment> assignments);

    @Override
    public int calculateNumberOfSlots(Seq<SlotAssignment> assignments){
        //code
    }

    @Override
    public void removeSlotAssignment(Seq<SlotAssignment> assignments, int index){
        //code
    }
}
public class DistanceAssignmentStrategy implements SlotAssignmentStrategy{
    private final Vec3 vec = new Vec3();
    private final FormationPattern form;

    public DistanceAssignmentStrategy(FormationPattern form){
        this.form = form;
    }
}
public class FreeSlotAssignmentStrategy implements SlotAssignmentStrategy{

    @Override
    public void updateSlotAssignments(Seq<SlotAssignment> assignments){
        // A very simple assignment algorithm: we simply go through
        // each assignment in the list and assign sequential slot numbers
        for(int i = 0; i < assignments.size; i++){
            assignments.get(i).slotNumber = i;
        }
    }

    @Override
    public int calculateNumberOfSlots(Seq<SlotAssignment> assignments){
        return assignments.size;
    }

    @Override
    public void removeSlotAssignment(Seq<SlotAssignment> assignments, int index){
        assignments.remove(index);
    }

}
```
BoundedSlotAssignmentStrategy có concrete: SoftRoleSlotAssignmentStrategy

```java
public class SoftRoleSlotAssignmentStrategy extends BoundedSlotAssignmentStrategy{
    //code
}
```
Factory Method:

Creator: FormationPattern

Concretecreator: CircleFormation, SquareFormation

Abstract Factory:

UnitController->AIController
Mindustry/core/src/mindustry/entities/units/UnitController.java

```java
public interface UnitController{
}
```
Mindustry/core/src/mindustry/ai/types
AIController->BuilderAI, DefenderAI, FlyingAI, FormationAI, GroundAI, HugAI, LogicAI, MinerAI, RepairAI

Facade:

facade: ContentList
Mindustry/core/src/mindustry/ctype/ContentList.jav

```java
public interface ContentList{
    /** This method should create all the content. */
    void load();
}
```
subsystems: Blocks, Bullets, Items, Liquids, Loadouts, PLanets, SectorPresets, StatusEffects, TechTree, UnitTypes, Weathers
Mindustry/core/src/mindustry/content

```java
public class Blocks implements ContentList{
    public static Block...
}
public class Bullets implements ContentList{
    public static BulletType...
}
public class Items implements ContentList{
    public static Item
    scrap, copper, lead, graphite, coal, titanium, thorium, silicon, plastanium,
    phaseFabric, surgeAlloy, sporePod, sand, blastCompound, pyratite, metaglass;
}
public class Loadouts implements ContentList{
    public static Schematic
    basicShard,
    basicFoundation,
    basicNucleus;

    @Override
    public void load(){
        basicShard = Schematics.readBase64...
    }
}
public class TechTree implements ContentList{
    static ObjectMap<UnlockableContent, TechNode> map = new ObjectMap<>();
    static TechNode context = null;

    public static Seq<TechNode> all;
    public static TechNode root;
    //code
}
public class Weathers implements ContentList{
    public static Weather
    rain,
    snow,
    sandstorm,
    sporestorm,
    fog,
    suspendParticles;

    @Override
    public void load(){
        snow = ...
        rain = ...
        sandstorm = ...
        sporestorm = ...
        fog = ...
        suspendParticles = ...
    }
}
```   
-> dễ dàng quản lý, điều hướng
