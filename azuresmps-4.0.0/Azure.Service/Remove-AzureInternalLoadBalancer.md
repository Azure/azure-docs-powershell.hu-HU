---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016475"
---
# Remove-AzureInternalLoadBalancer

## Áttekintés
Belső terheléselosztó konfiguráció eltávolítása.

## SZINTAXISA

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureInternalLoadBalancer** parancsmag eltávolítja a belső terheléselosztási konfigurációt egy Azure-szolgáltatásból.
Ha bármely végpont jelenleg a belső terheléselosztásra hivatkozik, ez a parancsmag nem tudja eltávolítani a konfigurációt.

## Példák

### 1. példa: belső terheléselosztó konfiguráció eltávolítása
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

Ez a parancs eltávolítja a ContosoService nevű szolgáltatás belső terheléselosztó konfigurációját.

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
Annak a szolgáltatásnak a neve, amelyből a parancsmag eltávolítja a belső terheléselosztást.

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

### Microsoft. WindowsAzure. commands. Utilities. Common. ManagementOperationContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureInternalLoadBalancer](./Add-AzureInternalLoadBalancer.md)

[Get-AzureInternalLoadBalancer](./Get-AzureInternalLoadBalancer.md)

[Új – AzureInternalLoadBalancerConfig](./New-AzureInternalLoadBalancerConfig.md)

[Set-AzureInternalLoadBalancer](./Set-AzureInternalLoadBalancer.md)


