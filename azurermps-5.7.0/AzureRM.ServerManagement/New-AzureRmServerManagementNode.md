---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: 498be36141d1a44d33cdcb351b92d5b6908071c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492180"
---
# New-AzureRmServerManagementNode

## Áttekintés
Kiszolgáló-kezelési csomópont létrehozása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByName
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObject
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **New-AzureRmServerManagementNode** parancsmag létrehoz egy Azure Server Management csomópontot.

## Példák

## PARAMÉTEREK

### -Számítógépnév
A felügyelt számítógép számítógépének a nevét adja meg.

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

### -Hitelesítő adatok
A Kiszolgálókezelő csomóponthoz való kapcsolat **PSCredential** -objektumát adja meg.
Hitelesítőadat-objektum beolvasásához használja az Get-Credential parancsmagot.
További információért írja be a következőt: `Get-Help Get-Credential` .

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
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

### -Gateway
A csomópontot kezelő átjárót adja meg.

Ezt a paramétert a *ResourceGroupName* , a *GatewayName* és a *hely* paraméter helyett használhatja.

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -GatewayName
A csomópontot elérő átjáró nevét adja meg.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Hely
Azt a helyet adja meg, ahol ez a parancsmag hozza létre a csomópontot.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Csomópontnév
A csomópont nevét adja meg.

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

### -ResourceGroupName
Annak az erőforrás csoportnak a nevét adja meg, amelyben a parancsmag létrehozta a csomópontot.

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

### -Címke
Az objektumhoz társított kulcs/érték párok

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Átjáró
Az "átjáró" paraméter elfogadja az "átjáró" típusú értéket a csővezetéken

## KIMENETEK

### Microsoft. Azure. Command. ServerManagement. Model. Node

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmServerManagementNode](./Get-AzureRmServerManagementNode.md)

[Remove-AzureRmServerManagementNode](./Remove-AzureRmServerManagementNode.md)


