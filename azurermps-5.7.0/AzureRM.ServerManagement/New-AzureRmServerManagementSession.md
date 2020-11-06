---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 7d8b2e02e5683f58eee06de1993f6ea0d4ecfac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492183"
---
# New-AzureRmServerManagementSession

## Áttekintés
Kiszolgáló-kezelési munkamenet létrehozása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByName
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNode
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmServerManagementSession** parancsmag Azure Server Management-munkamenetet hoz létre.

## Példák

## PARAMÉTEREK

### -Hitelesítő adatok
A Kiszolgálókezelő-munkamenethez kapcsolódó kapcsolat **PSCredential** -objektumát adja meg.
Hitelesítőadat-objektum beolvasásához használja az Get-Credential parancsmagot.
További információért írja be a következőt: `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Node
Azt a csomópontot adja meg, amelyre a parancsmag létrehozta a munkamenetet.

Ezt a paramétert a *ResourceGroupName* és a *csomópontnév* paraméter helyett használhatja.

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Csomópontnév
Annak a csomópontnak a nevét adja meg, amelyhez ez a parancsmag létrehoz egy munkamenetet.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a csomópontnak az erőforrás csoportját adja meg, amelyre a parancsmag létrehozta a munkamenetet.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Munkamenet
Itt adhatja meg a munkamenethez használni kívánt nevet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Csomópont
A "Node" paraméter elfogadja a "csomópont" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. ServerManagement. Model. Session

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

