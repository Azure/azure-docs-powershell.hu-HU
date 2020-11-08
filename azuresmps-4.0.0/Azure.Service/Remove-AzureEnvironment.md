---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016477"
---
# Remove-AzureEnvironment

## Áttekintés
Azure-környezet törlése a Windows PowerShellből

## SZINTAXISA

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
A **Remove-AzureEnvironment** parancsmag egy Azure-környezetet töröl a központi profilból, így a Windows PowerShell nem találja.
Ez a parancsmag nem törli a környezetet a Microsoft Azure rendszerből, illetve semmilyen módon nem változtatja meg a tényleges környezetet.

Azure-környezet: a Microsoft Azure független központi üzembe állítása, például a AzureCloud a globális Azure-és a AzureChinaCloud által üzemeltetett Azure-alapú 21Vianet Kínában.
A helyszíni Azure-környezeteket az Azure Pack és a WAPack parancsmagok használatával is létrehozhatja.
További tudnivalókat az [Azure Pack (csomag](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ) című témakörben talál https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

## Példák

### Példa 1: környezet törlése
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

Ez a parancs törli a ContosoEnv-környezetet a Windows PowerShellből.

### 2. példa: több környezet törlése
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

Ez a parancs törli azokat a környezeteket, amelyek neve "contoso" néven kezdődik a Windows PowerShellben.

## PARAMÉTEREK

### -Force
Letiltja a megerősítési kérdést.

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

### -Name (név)
Az eltávolítandó környezet nevét adja meg.
Ehhez a paraméterhez szükség van.
Ez a paraméterérték megkülönbözteti a kis-és nagybetűket.
A helyettesítő karakterek nem engedélyezettek.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
A parancsmagot tulajdonság nevében, de nem érték szerint is beírhatja.

## KIMENETEK

### Nincs vagy System. Boolean
Ha a *PassThru* paramétert használja, ez a parancsmag logikai értéket ad eredményül.
Ellenkező esetben nem ad vissza semmilyen eredményt.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


