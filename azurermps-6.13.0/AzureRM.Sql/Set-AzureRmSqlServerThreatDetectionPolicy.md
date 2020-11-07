---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5e9a4e25d54be7282e4d2f0b5f83471140241c58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672440"
---
# Set-AzureRmSqlServerThreatDetectionPolicy

## Áttekintés
Veszélyforrás-észlelési házirendet állít be a kiszolgálón.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzureRmSqlServerThreatDetectionPolicy** parancsmag fenyegetés-észlelési házirendet állít be egy Azure SQL Serveren.
A fenyegetések észlelésének engedélyezéséhez a kiszolgálón engedélyeznie kell a naplózási házirendet.
A parancsmag használatához adja meg a *ResourceGroupName* és a kiszolgálónév paramétert a kiszolgáló azonosítójának megadásához.

## Példák

### 1. példa: az adatbázis veszélyforrás-észlelési házirendjének beállítása
```
PS C:\>Set-AzureRmSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

Ez a parancs beállítja a Server01 nevű kiszolgáló veszélyforrás-észlelési házirendjét.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EmailAdmins
Azt adja meg, hogy a fenyegetés észlelése házirend a rendszergazdákat e-mailben használja-e.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExcludedDetectionType
A házirendből kizárandó észlelési típusokból álló tömböt adja meg.
A paraméter elfogadható értékei a következők:
- Sql_Injection
- Sql_Injection_Vulnerability
- Access_Anomaly
- Nincs

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationRecipientsEmails
A házirend által küldött e-mail-címek pontosvesszővel elválasztott listáját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a neve, amelyhez a kiszolgáló tartozik.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
A naplók adatmegőrzési napjainak száma

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kiszolgálónév
A kiszolgáló nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
A használandó tárterület-fiók nevét adja meg. A helyettesítő karakterek nem engedélyezettek. Ehhez a paraméterhez nincs szükség. Ha ezt a paramétert nem jeleníti meg, a parancsmag az adatbázis veszélyforrások észlelési házirendjének részeként megadott tárolási fiókot fogja használni. Ha ez az első alkalom, hogy egy adatbázis-theat-észlelési házirend van definiálva, és ez a paraméter nem jelenik meg, a parancsmag nem fog működni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

### Microsoft. Azure. Command. SQL. ThreatDetection. Model. DetectionType []

### System. null ' 1 [[System. UInt32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

## KIMENETEK

### Microsoft. Azure. Command. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSqlServerThreatDetectionPolicy](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[Remove-AzureRmSqlServerThreatDetectionPolicy](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[SQL-adatbázis dokumentációja](https://docs.microsoft.com/azure/sql-database/)
