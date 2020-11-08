---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016340"
---
# Get-AzureInternalLoadBalancer

## Áttekintés
A belső terheléselosztó konfiguráció részleteit kapja meg.

## SZINTAXISA

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureInternalLoadBalancer** parancsmag az Azure-szolgáltatások belső terheléselosztási konfigurációjának részleteit kapja meg.

## Példák

### Példa 1: adatok beszerzése belső terheléselosztó rendszerhez
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

Ez a parancs a ContosoService nevű szolgáltatást a **Get-AzureService** parancsmag használatával kapja.
A parancs a csővezeték-kezelő segítségével átadja ezt a szolgáltatást az aktuális parancsmagnak.
Az aktuális parancsmag részletesen részletezi a szolgáltatás belső terheléselosztását.

## PARAMÉTEREK

### -InformationAction
Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.

A paraméter elfogadható értékei a következők:

- Folytassa
- Mellőzése
- Érdeklődni
- SilentlyContinue
- állj
- Felfüggesztheti

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Egy információs változót ad meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Szolgáltatásnév
Annak a szolgáltatásnak a nevét adja meg, amelyhez ez a parancsmag részletezni kíván egy belső terheléselosztást.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. Command. ServiceManagement. Model. InternalLoadBalancerContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureInternalLoadBalancer](./Add-AzureInternalLoadBalancer.md)

[Get-AzureService](./Get-AzureService.md)

[Új – AzureInternalLoadBalancerConfig](./New-AzureInternalLoadBalancerConfig.md)

[Remove-AzureInternalLoadBalancer](./Remove-AzureInternalLoadBalancer.md)

[Set-AzureInternalLoadBalancer](./Set-AzureInternalLoadBalancer.md)


