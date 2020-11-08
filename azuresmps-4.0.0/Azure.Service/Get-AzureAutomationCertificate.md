---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015663"
---
# Get-AzureAutomationCertificate

## Áttekintés

Azure automatizálási tanúsítványt kap.

## SZINTAXISA

### ByAll (alapértelmezett)
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByCertificateName
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **Get-AzureAutomationCertificate** parancsmag egy vagy több Microsoft Azure automatizálási tanúsítványt kap.
Alapértelmezés szerint minden tanúsítvány visszaadva van.
Egy adott tanúsítvány beszerzéséhez adja meg a nevét.

## Példák

### Példa 1: az összes tanúsítvány beszerzése
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

Ez a parancs a Contoso17 nevű Azure Automation fiók minden tanúsítványát beolvassa.

### 2. példa: tanúsítvány beszerzése
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

Ez a parancs a MyUserCertificate nevű tanúsítványt kapja meg.

## PARAMÉTEREK

### -AutomationAccountName
A tanúsítványt használó automatizálási fiók nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A beolvasandó tanúsítvány nevét adja meg.

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. CertificateInfo

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureAutomationCertificate](./New-AzureAutomationCertificate.md)

[Remove-AzureAutomationCertificate](./Remove-AzureAutomationCertificate.md)

[Set-AzureAutomationCertificate](./Set-AzureAutomationCertificate.md)


