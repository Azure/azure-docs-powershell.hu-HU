---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016244"
---
# Move-AzureDeployment

## Áttekintés
A termelés és a megállóhelyek bevezetésének felcserélése

## SZINTAXISA

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Leírás
A **Move-AzureDeployment** parancsmag a bevezetések virtuális IP-címét a termelés és az átmeneti környezetekben cseréli.
Ez a parancsmag egy olyan üzembe állítást cserél, amely jelenleg az átmeneti környezetben fut a termelési környezetbe, valamint egy olyan üzembe állítást, amely a termelési környezetben fut az átmeneti környezetben.
Ha a bevezetést a bevezetési környezetben telepítette, és nem működik a környezet, a parancsmag a bevezetést a termelésbe helyezi.
Ha van egy központi telepítési környezet, és nincs bevezetése az átmeneti környezetben, a parancsmag nem működik.

## Példák

### 1. példa: szolgáltatások bevezetésének cseréje
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

Ez a parancs a ContosoService nevű szolgáltatás üzembe helyezését a termelés és az átmeneti környezetek között cseréli.

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
Annak a szolgáltatásnak a nevét adja meg, amelynek a parancsmagja a termelést és az átmeneti telepítési példányokat felcseréli.

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

### ManagementOperationContext

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Új – AzureDeployment](./New-AzureDeployment.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Set-AzureDeployment](./Set-AzureDeployment.md)


