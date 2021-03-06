# Araştırma Ödevleri:

- [Araştırma Projesi 1 - Lateinit](#1)
- [Araştırma Projesi 2 - Tools Namespace](#2)
- [Araştırma Projesi 3 - Font family XML](#3)
- [Araştırma Projesi 4 - Property Animation](#4)



### <a name="1"></a> Araştırma Projesi 1

- Lateinit neden kullanıyoruz?
- Lateinit kullanımından bahseder misiniz?
- Lateinit için bir örnek kullanım gösterir misiniz ?
### Cevap:
Lateinit geç başlatma anlamına gelir. Yapıcıda bir değişken başlatmak istemiyorsanız, onu daha sonra başlatmak istiyorsanız ve kullanmadan önce başlatmayı garanti edebiliyorsanız, o değişkeni lateinit anahtar kelimesiyle bildirin. Başlatılana kadar bellek ayırmaz.
Lateinit değişkeni için val kullanamazsınız , çünkü daha sonra başlatılacaktır. Ayrıca değişkeni kullanmadan önce değişkeni başlattığınızdan emin olmalısınız, aksi takdirde çalışma zamanında istisna atar.Lateinit'i Int, Long vb. gibi ilkel tür özellikleri için kullanamazsınız.
Bir lateinit özelliğine, başlatılmadan önce erişmek, erişilmekte olan özelliği ve başlatılmamış olduğu gerçeğini açıkça tanımlayan özel bir istisna atar.

class LoginFragment : Fragment() {

    private lateinit var usernameEditText: EditText
    private lateinit var passwordEditText: EditText
    private lateinit var loginButton: Button
    private lateinit var statusTextView: TextView

    override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
        super.onViewCreated(view, savedInstanceState)

        usernameEditText = view.findViewById(R.id.username_edit_text)
        passwordEditText = view.findViewById(R.id.password_edit_text)
        loginButton = view.findViewById(R.id.login_button)
        statusTextView = view.findViewById(R.id.status_text_view)
    }

    
}

### <a name="2"></a> Araştırma Projesi 2


- Layout dizini içinde xml dosyalarımız için kullandığımız namespace nedir ?
- Neden kullanılmaktadır ?
- Nasıl kullanılmalıdır ?
- Bir adet Tools (tools namespace) attribute kullanımını gösterir misiniz ? 

### Cevap:

Uygulama geliştirirken tasarım tarafında yapılan değişikliklerin çıktısını uygulamayı çalıştırmadan anında görebilmek tools attribute
sayesinde olur.

<img src="https://user-images.githubusercontent.com/56538177/163602178-4f8610ec-4aed-4b12-99c6-1c43f0de9968.png"  width="550" height="500">
    
## <a name="3"></a> Araştırma Projesi 3

- Font family dosyası nasıl oluşturulup kullanıyoruz? 
- Neden belirttiğiniz şekilde kullanımı tercih ediyoruz?

P.S. [Bu linkten](https://developer.android.com/guide/topics/ui/look-and-feel/fonts-in-xml ) faydalanarak font family projenizde deneyebilirsiniz.

Font dosyasını internet sitesinden indiririz.İndirdiğimiz dosyayı zip’ten çıkartıp ve fonts klasörürünün içindeki fontawesome-webfont.ttf isimli font dosyasını Android projemizin Assets klasörüne fonts isminde bir klasör yaratıp ilgili font dosyasını oluşturmuş olduğumuz klasöre kopyalarız.

Android uygulamalarımızı geliştirirken custom fontlar kullanmak isteyebiliriz işte bu fontları font klasörü içine atmamız gerekmektedir.


## <a name="4"></a> Araştırma Projesi 4

- Property Animation ile ilgili olarak objectAnimator ile animator arasındaki farkı kısaca açıklayınız

P.S. [Bu linkten](https://developer.android.com/guide/topics/resources/animation-resource#Property) faydalanabilirsiniz.    

ObjectAnimator belirli bir süre boyunca bir nesnenin belirli bir özelliğini canlandırır. 

Animator,başlatılabilen, sonlandırılabilen ve kendilerine AnimatorListener eklenmiş animasyonlar için temel destek sağlayan üst sınıftır.
