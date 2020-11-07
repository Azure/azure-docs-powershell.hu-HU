---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 1eafc934777809d7fd4041496b004ea682e97910
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843466"
---
# Get-AzDeploymentOperation

## Áttekintés
Üzembe állítási művelet

## SZINTAXISA

### GetByDeploymentName (alapértelmezett)
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzDeploymentOperation** parancsmag a központi üzembe állítás részét képező összes műveletet felsorolja, így könnyebben megtalálhatja és megadhatja az adott üzembe állítással kapcsolatos pontos műveleteket.
A válasz és a kérés tartalma is megjeleníthető az egyes üzembe állítási műveletekhez.
Ez a cikk a portálon található központi verzió központi telepítéséhez szükséges információkat ismerteti.

A kérelem és a válasz tartalmának beszerzéséhez engedélyezze a beállítást, ha a bevezetést az **új AzDeployment-** on keresztül küldi el.
Előfordulhat, hogy az erőforrás-tulajdonságokban vagy a **listKeys** -műveletekben használt jelszavakat, például a központi telepítési műveletek lekérése után visszaadott jelszavakat is naplózhatja és megjelenítheti.
A beállításról és annak engedélyezéséről további információt a ARM-sablonok bevezetésének New-AzDeployment és hibakeresése című témakörben talál.

## Példák

### Központi telepítői műveletek beszerzése a központi telepítő nevében
```
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

A "teszt" nevű központi üzembe állítási művelet a jelenlegi előfizetési tartományban

### Üzembe állítási műveletek beszerzése és üzembe állítása
```
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

Ez a parancs beilleszti a "teszt" műveletet a jelenlegi előfizetési tartományba, és beilleszti a központi üzembe állítási műveleteket.

## PARAMÉTEREK

### -ApiVersion
Ha be van jelölve, akkor az erőforrás-szolgáltató API-nak a verziószámát adja meg.
Ha nem adja meg, akkor az API-t a program automatikusan a legújabb verzióként határozza meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentName
A központi telepítő neve.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentObject
A központi telepítő objektum.

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperationId
A központi telepítő műveleti azonosító.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Ha be van állítva, akkor az azt jelzi, hogy a parancsmagnak az API előzetes verziójának kell lennie, amikor automatikusan meghatározza, hogy melyik verziót használja.

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

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String
System. null ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
