---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492200"
---
# Get-AzureRmReservation

## Áttekintés
Az s beszerzése `Reservation` adott foglalási sorrendben

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### CommandLine (alapértelmezett)
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### PipeObject
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## Leírás
`Reservation`Az s betű egyetlenen belül `ReservationOrder`

## Példák

### Példa 1
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

`Reservation`A megadott listában lévő EK `ReservationOrder`

### 2. példa
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

Konkrét `Reservation` részleteket kaphat.

## PARAMÉTEREK

### -ReservationId
A `Reservation` megtekinteni kívánt azonosító

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrder
Pipe Object paraméter `ReservationOrder`

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReservationOrderId
Az adott azonosítójú azonosítót `ReservationOrder` tartalmazó azonosító `Reservation` . Szükséges.

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrderPage
Pipe Object paraméter `ReservationOrder`

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
Microsoft. Azure. commands. Reservations. models. PSReservationOrder Microsoft. Azure. commands. Reservations. models. PSReservationOrderPage

## KIMENETEK

### Microsoft. Azure. commands. Reservations. models. PSReservationPage
Microsoft. Azure. commands. Reservations. models. PSReservation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

