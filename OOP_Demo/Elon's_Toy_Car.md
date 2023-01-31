Hướng dẫn

Trong bài tập này, bạn sẽ phải hiển thị thông số của một chiếc xe ô tô điều khiển từ xa.

Xe khởi động khi đầy (100%) ắc quy. Mỗi lần xe di chuyển, nó sẽ đi được 20 mét và tiêu hao một phần trăm pin.

Chiếc xe điều khiển từ xa có màn hình LED lạ mắt hiển thị hai thông tin:

   - Tổng quãng đường nó đã lái, được hiển thị dưới dạng: ``"Driven /<METERS/> meters"``.

   - Lượng pin còn lại, được hiển thị dưới dạng: ``"Battery at /<PERCENTAGE/>%"``.

Nếu pin ở mức 0%, bạn không thể lái xe nữa và màn hình pin sẽ hiển thị "Battery empty".

Bạn cần phải hoàn thiện class ``ElonsToyCar`` để thực hiện các yêu cầu sau.

1. Mua ô tô điều khiển từ xa mới toanh
    Thực hiện phương thức ( static ) ``ElonsToyCar.buy()`` để trả về một phiên bản ô tô được điều khiển từ xa hoàn toàn mới:

    ```Java
        ElonsToyCar car = ElonsToyCar.buy();
    ```

2. Hiển thị quãng đường đã đi
    Thực hiện phương thức ``ElonsToyCar.distanceDisplay()`` để trả về khoảng cách như được hiển thị trên màn hình LED:

    ```Java
        ElonsToyCar car = ElonsToyCar.buy();
        car.distanceDisplay();
        // => "Driven 0 meters"
    ```

3. Hiển thị phần trăm pin

    Thực hiện phương thức ``ElonsToyCar.batteryDisplay()`` trả về phần trăm pin như hiển thị trên màn hình LED:

    ```Java
        ElonsToyCar car = ElonsToyCar.buy();
        car.batteryDisplay();
        // => "Battery at 100%"
    ```

4. Cập nhật số mét đã đi khi lái xe

    Thực hiện phương thức ``ElonsToyCar.drive()`` cập nhật số mét đã lái:


    ```Java
        ElonsToyCar car = ElonsToyCar.buy();
        car.drive();
        car.drive();
        car.distanceDisplay();
        // => "Driven 40 meters"
    ```

5. Cập nhật phần trăm pin khi lái xe

    Cập nhật phương thức ``ElonsToyCar.drive()`` cập nhật phần trăm pin:

    ```Java
        ElonsToyCar car = ElonsToyCar.buy();
        car.drive();
        car.drive();
        car.batteryDisplay();
        // => "Battery at 98%"
    ```

6. Tránh lái xe khi hết pin

    Cập nhật phương thức ``ElonsToyCar.drive() ``để không tăng quãng đường đã đi cũng như không giảm phần trăm pin khi hết pin (ở mức 0%):

    ```Java
        ElonsToyCar car = ElonsToyCar.buy();

        // Drain the battery
        // ...

        car.distanceDisplay();
        // => "Driven 2000 meters"

        car.batteryDisplay();
        // => "Battery empty"
    ```
