---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466544"
---
# Get-AzDeploymentOperation

## SYNOPSIS
Telepítési művelet

## SZINTAXIS

### GetByDeploymentName (alapértelmezett)
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentObject
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzDeploymentOperation** parancsmag felsorolja azokat a műveleteket, amelyek egy központi telepítés részét képezték, hogy ön azonosítsa és további információt nyújtson az adott telepítésben sikertelen műveletekről.
Emellett az egyes telepítési műveletek válaszát és kérési tartalmát is meg tudja mutatni.
Ezek ugyanazok az információk, amelyek a portál telepítési részleteiben is megegyezik.

A kérés és a választartalom lekéréséhez engedélyezze a beállítást, amikor a **New-AzDeployment** szolgáltatáson keresztül beküld egy központi telepítést.
Naplózhat és felfedhet olyan titkosságokat, például az erőforrástulajdonságban vagy a **listKeys** műveletben használt jelszavakat, amelyek az üzembe helyezési műveletek lekérésekor ad vissza.
A beállításról és annak engedélyezéséről további információt a New-AzDeployment és ARM sablontelepítések

## PÉLDÁK

### 1. példa: Telepítési műveletek lekérte a telepítés nevét
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

Az aktuális előfizetési hatókörű "teszt" névvel üzembe helyezési műveletet kap.

### 2. példa: Telepítési és telepítési műveletek lekérte
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

Ez a parancs a központi telepítés "tesztelését" kapja meg az aktuális előfizetés hatókörében, és be is szerezze a telepítési műveleteket.

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentName
A telepítés neve.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentObject
A telepítőobjektum.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperationId
A telepítési művelet azonosítója.

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Ha be van állítva, az azt jelzi, hogy a parancsmagnak előzetes API-verziókat kell használnia, amikor automatikusan meghatározza, hogy melyik verziót használja.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## KIMENETEK

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
