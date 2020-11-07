---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: ff3cdb549835ceb4689ee5be8569b61ffa89538d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670968"
---
# Set-AzDeploymentManagerServiceTopology

## Áttekintés
Frissíti a szolgáltatási topológiát.

## SZINTAXISA

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzDeploymentManagerServiceTopology** parancsmag a megadott szolgáltatási topológia objektummal frissíti a szolgáltatási topológiát.
A parancsmag a frissített szolgáltatási topológia objektumot számítja ki.

## Példák

### Példa 1
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

Ez a parancs frissíti a szolgáltatási topológiát, amelynek a neve és a ResourceGroup megegyeznek a $serviceTopologyObject neve és ResourceGroupName tulajdonságaival.
A parancs a frissített szolgáltatás topológiája objektumot ad eredményül.

## PARAMÉTEREK

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -InputObject
A szolgáltatás topológiája objektum.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource

## KIMENETEK

### Microsoft. Azure. Command. DeploymentManager. models. PSServiceTopologyResource

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
