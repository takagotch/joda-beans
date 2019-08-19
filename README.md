### joda-beans
---
https://www.joda.org/joda-beans/

https://github.com/JodaOrg/joda-beans

```java
@BeanDefinition
public final class Foo implements Bean {
  @PropertyDefinition
  private String forename;
  
  @PropertyDefinition(validate = "notNull")
  private String surname;
  
  @PropertyDefinition
  private Address address;
}
```

```java
FixedRateSwapLeg payLeg = FixedRateSwapLeg.builder()
  .accrualPeriod(PeriodicScheduleDefn.buildr()
    .startDate(LocalDate.of(2014, 9, 12))
    .endDate(LocalDate.of(2021, 9, 12))
    .frequency(Frequency.P6M)
    .businessDayAdjustment(BusinessDayConventions.MODIFIED_FOLLOWING)
    .startDateBusinessDayAdjustment(BusinessDayAdjustment.NONE)
    .build())
  .calculation(FixedRateCalculation.builder()
    .notional(CurrencyAmount.of(Currency.USD, 100_000_000))
    .dayCount(DayCounts.THIRTY_U_360)
    .build())
  .build();

```

```
```
