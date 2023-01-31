Hướng dẫn

Trong bài tập này, bạn đang chơi một trò chơi nhập vai có tên là "Pháp sư và Chiến binh", trò chơi này cho phép bạn đóng vai Pháp sư hoặc Chiến binh.

Có các quy tắc khác nhau dành cho Chiến binh và Pháp sư để xác định số điểm sát thương mà họ gây ra.

Đối với một Chiến binh, có các quy tắc như sau :

- Gây 6 điểm sát thương nếu đối phương mà họ đang tấn công không dễ bị tổn thương

- Gây 10 điểm sát thương nếu đối phương mà họ đang tấn công dễ bị tổn thương

Đối với một Pháp sư, có các quy tắc như sau :

- Gây 12 điểm sát thương nếu Pháp sư chuẩn bị trước một câu thần chú

- Gây 3 điểm sát thương nếu Pháp sư không chuẩn bị bùa chú trước

Nói chung, Võ sĩ không bao giờ dễ bị tổn thương. Tuy nhiên, Pháp Sư rất dễ bị tổn thương nếu chưa chuẩn bị bùa chú.

Bạn có sáu nhiệm vụ hoạt động với các chiến binh Chiến binh và Pháp sư.

1. Diễn tả một Võ sĩ

    Ghi đè phương thức ``toString()`` trên lớp Fighter để trả về mô tả Võ sĩ, được định dạng là "Fighter is a <FIGHTER_TYPE>".

    ```Java
        Fighter warrior = new Warrior();
        warrior.toString();
        // => "Fighter is a Warrior"
    ```

2. Làm cho Võ sĩ không dễ bị tấn công theo mặc định

    Đảm bảo rằng phương thức ``Fighter.isVulnerable()`` luôn trả về false.

    ```Java
        Fighter warrior = new Warrior();
        warrior.isVulnerable();
        // => false
    ```

3. Cho phép Pháp sư chuẩn bị một câu thần chú

    Viết phương thức ``Wizard.prepareSpell() `` cho phép Pháp sư chuẩn bị trước một câu thần chú.

    ```Java
        Wizard wizard = new Wizard();
        wizard.prepareSpell();
    ```

4. Pháp Sư sơ hở khi chưa chuẩn bị bùa chú

    Đảm bảo rằng phương thức ``isVulnerable()`` trả về true nếu Pháp sư không chuẩn bị câu thần chú; nếu không, hãy trả lại false.

    ```Java
        Fighter wizard = new Wizard();
        wizard.isVulnerable();
        // => true
    ```

5. Tính điểm sát thương cho Pháp Sư

    Viết phương thức ``Wizard.damagePoints()`` trả lại điểm sát thương đã gây ra: 12 điểm sát thương khi đã chuẩn bị phép thuật, 3 điểm sát thương khi không chuẩn bị.

    ```Java
        Wizard wizard = new Wizard();
        Warrior warrior = new Warrior();

        wizard.prepareSpell();
        wizard.damagePoints(warrior);
        // => 12
    ```

6. Tính điểm sát thương cho Chiến binh

    Viết phương thức `` Warrior.damagePoints()`` hoàn trả điểm sát thương gây ra: 10 điểm sát thương khi mục tiêu dễ bị tổn thương, 6 điểm sát thương khi không.

    ```Java
        Warrior warrior = new Warrior();
        Wizard wizard = new Wizard();

        warrior.damagePoints(wizard);
        // => 10
    ```
