# Kullanıcı Girişi Ödevi
* Kullanıcı adı 'patika' ve şifresi 'java123' olan bir kullanıcı girişi ekranı yapıldı.
* Ekranda hatalı şifre sonrası kullanıcıya şifresini değiştirmek isteyip istemediğini soran bir sayfa açılır.
* Kullanıcı şifresini değiştirmek istemezse giriş sonlandırılır.
* Seçimi farklı girerse hata mesajı verilir.
* Şifresini değiştirmek ister ise yeni şifresi ekrana kullanıcı tarafından girilir.
* Eğer ki yeni şifresi eski şifresi ile aynı ise ekrana hata mesajı verilir.

```
import java.util.Scanner;

public class KullaniciGirisi {
    public static void main(String[] args) {
        String userName, password, sifirlama, newPassword;

        Scanner input = new Scanner(System.in);

        System.out.print("Kullanıcı Adınız :");
        userName = input.nextLine();
        System.out.print("Şifrenizi Giriniz :");
        password = input.nextLine();

        if (userName.equals("patika")) {
            if (password.equals("java123")) {
                System.out.print("Giriş Yaptınız !");
            }
            else {
                System.out.println("Hatalı Giriş Yaptınız");
                System.out.print("Şifrenizi sıfırlamak istiyorsanız ekrana \'yes\' yazın."+
                        "\nSıfırlamak istemiyorsanız ekrana \'no\' yazınız.");

                sifirlama=input.nextLine();

                if(sifirlama.equals("no")){
                    System.out.print("Giriş Sonlandırıldı.");
                }
                else if(sifirlama.equals("yes")){
                    System.out.print("Yeni Şifrenizi Giriniz :");
                    newPassword=input.nextLine();

                    if(newPassword.equals("java123")){
                        System.out.print("Hatalı Şifre Seçimi");
                    }
                    else{
                        System.out.print("Şifrenizi Başarıyla Değiştirdiniz.");
                    }
                }else{
                    System.out.print("Hatalı Seçim Yaptınız !");
                }
            }


        }else{
            System.out.print("Böyle Bir Kullanıcı Adı Bulunamadı");
        }
    }
}
```

# Patika Profilim
***
<a href="https://academy.patika.dev/profile">Patika Profilim</a>