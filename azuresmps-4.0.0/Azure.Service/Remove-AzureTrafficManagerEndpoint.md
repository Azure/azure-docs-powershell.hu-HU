---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016092"
---
# Remove-AzureTrafficManagerEndpoint

## Áttekintés
Végpont eltávolítása a forgalomirányító profiljából.

## SZINTAXISA

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureTrafficManagerEndpoint** parancsmag a Microsoft Azure Traffic Manager-profilból távolítja el a végpontot.
Miután eltávolított egy végpontot, átadja az eredményt a **set-AzureTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.
Ez a parancsmag az Azure-hoz csatlakozik a módosítások mentéséhez.

## Példák

### Példa 1: végpont eltávolítása egy profilból
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

Az első parancs a **Get-AzureTrafficManagerProfile** parancsmagot használja a ContosoProfile nevű profil beolvasásához, majd a $TrafficManagerProfile változóban tárolja.

A második parancs eltávolítja azt a végpontot, amelynek a tartományneve Contoso02App.cloudapp.net a $TrafficManagerProfileban tárolt forgalomirányítási profilból.
A parancs átadja a profil objektumnak a **set-AzureTrafficManagerProfile** parancsmagot az Azure-hoz való csatlakozáshoz a módosítások mentéséhez.

## PARAMÉTEREK

### -Tartománynév
Az eltávolítandó végpont tartománynevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható. Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

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

### -TrafficManagerProfile
Annak a Traffic Manager-profil objektumnak a meghatározása, amelyből el szeretné távolítani a végpontot.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

### Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition
Ez a parancsmag a Traffic Manager profil objektumát hozza létre, amely a frissített profillal kapcsolatos információkat tartalmazza.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


