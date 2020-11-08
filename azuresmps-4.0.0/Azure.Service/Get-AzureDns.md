---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015646"
---
# Get-AzureDns

## Áttekintés
Beolvassa az Azure-alapú központi környezet DNS-beállításait.

## SZINTAXISA

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Get-AzureDns** parancsmag az Azure-alapú központi telepítéséhez szükséges DNS-beállításokat kapja meg.
A parancsmag a DNS-kiszolgáló rövid nevét és IP-címét adja eredményül egy DNS-beállítási objektumban.

## Példák

### Példa 1: DNS-beállítások beszerzése
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

Ez a parancs a **Get-AzureDeployment** parancsmagot használja a ContosoService nevű szolgáltatás termelésének beszerzéséhez.
A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.
Az aktuális parancsmag a DNS-beállításokat kapja meg.

## PARAMÉTEREK

### -DnsSettings
Egy **DnsSettings** -objektumot ad meg.

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureDns](./Add-AzureDns.md)

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Új – AzureDns](./New-AzureDns.md)

[Remove-AzureDns](./Remove-AzureDns.md)

[Set-AzureDns](./Set-AzureDns.md)


