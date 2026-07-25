## Məlumatların Hazırlanması

- `orders`, `order_items` və `order_reviews` datasetləri **order_id** sütunu əsasında birləşdirildi.
- Analizin daha dəqiq olması üçün yalnız **"delivered"** statusuna malik sifarişlər saxlanıldı. Filtrləmədən sonra datasetdə təxminən **96.5 min** sifariş qaldı.
- Tarix sütunları `datetime` formatına çevrildi.
- Aylıq analiz aparmaq üçün **YearMonth** sütunu yaradıldı.

---

## Cohort Analizi

- Hər bir müştərinin etdiyi ilk sifariş ayı müəyyən edilərək **CohortMonth** sütunu yaradıldı.
- Daha sonra sifariş ayı ilə ilk sifariş ayı arasındakı fərq hesablanaraq **CohortIndex** sütunu yaradıldı.
- Müştərilərin zamanla platformaya geri qayıtma davranışını qiymətləndirmək üçün Cohort Pivot və Retention cədvəlləri hazırlandı.

### Əsas nəticələr

- Ən kiçik cohort **2016-cı ilin sentyabr ayına** aiddir və **3 müştəridən** ibarətdir.
- Ən böyük cohort isə **2018-ci ilin mart ayıdır** və təxminən **6.947 müştərini** əhatə edir.
- Cohort analizi göstərir ki, ilk alışdan sonra müştərilərin platformaya geri qayıtma faizi sürətlə azalır.
- İlk aydan ikinci aya keçiddə orta **Retention Rate cəmi 5.2%** olmuşdur. Bu isə müştərilərin böyük hissəsinin yalnız bir dəfə alış etdiyini göstərir.
- Nəticələr Braziliya elektron ticarət bazarında **müştəri itkisinin (Customer Churn)** yüksək olduğunu göstərir.

---

## Çatdırılma Müddətinin Analizi

- Çatdırılma müddəti `order_delivered_customer_date` və `order_purchase_timestamp` sütunları arasındakı fərq əsasında hesablandı.
- Sifarişlərin **orta çatdırılma müddəti 12.01 gün** olaraq müəyyən edildi.

---

## Müştəri Məmnuniyyətinin Analizi

- Müştərilərin verdiyi **orta qiymətləndirmə (Review Score) 4.09 bal** olmuşdur.
- Çatdırılma müddəti ilə müştəri qiymətləndirməsi arasında **-0.30 korrelyasiya** hesablandı.
- Bu nəticə göstərir ki, çatdırılma müddəti artdıqca müştərilərin verdiyi qiymətlər azalma meyli göstərir.
- Deməli, çatdırılma sürəti müştəri məmnuniyyətinə təsir edən vacib amillərdən biridir.

- -----------------------------------------------------------------
 Data Preparation

- Merged **three datasets** (`orders`, `order_items`, and `order_reviews`) using **`order_id`** as the primary key.
- Filtered the dataset to include only **delivered orders**, resulting in approximately **96.5K completed orders** for analysis.
- Converted purchase and delivery timestamps into datetime format for time-based analysis.
- Created a **YearMonth** column to support monthly cohort analysis.

---

## Cohort Analysis

- Identified each customer's **first purchase month**, stored as **CohortMonth**.
- Calculated **CohortIndex**, representing the number of months elapsed since a customer's first purchase.
- Built a cohort retention matrix to analyze repeat purchasing behavior over time.

### Key Findings

- The **smallest cohort** was **September 2016**, consisting of **3 customers**.
- The **largest cohort** was **March 2018**, with approximately **6.947 customers**.
- Customer retention drops sharply after the first purchase.
- The average **Month 1 → Month 2 retention rate is only 5.2%**, indicating that only a small percentage of customers return for another purchase.
- Overall, the cohort analysis suggests a **high customer churn rate**, where most customers purchase only once and do not return.

---

## Delivery Performance Analysis

- Calculated the delivery duration as the difference between **order_delivered_customer_date** and **order_purchase_timestamp**.
- The **average delivery time** is **12.01 days**.

---

## Customer Satisfaction Analysis

- The **average review score** is **4.09 / 5**, indicating generally positive customer satisfaction.
- The correlation between **delivery time** and **review score** is **-0.30**, suggesting a **moderate negative relationship**.
- Customers tend to leave lower ratings as delivery time increases.
- Delivery speed appears to be an important factor influencing the overall shopping experience.

---

