---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: 6fbef2bcedf4de93cd816f6a4702ee01df10d17f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921474"
---
# Set-AzAutomationCredential

## SYNOPSIS
Módosítja az automatizálási hitelesítő adatokat.

## SZINTAXIS

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzAutomationCredential** parancsmag módosítja a hitelesítő adatokat **PSCredential** objektumként az Azure Automationben.

## PÉLDÁK

### 1. példa: Hitelesítő adatok frissítése
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

Az első parancs hozzárendel egy felhasználónevet a $User változóhoz.
A második parancs egy egyszerű szöveges jelszót biztonságos karakterláncsá alakít át a ConvertTo-SecureString parancsmag használatával.
A parancs az objektumot a $Password tárolja.
A harmadik parancs létrehoz egy hitelesítő adatokat a $User és $Password alapján, majd tárolja azt a $Credential változóban.
Az utolsó parancs módosítja a ContosoCredential nevű automatizálási hitelesítő adatokat a hitelesítő adatok $Credential.

## PARAMETERS

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja módosítja a hitelesítő adatait.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -Leírás
Megadja annak a hitelesítő adatnak a leírását, amit ez a parancsmag módosít.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Megadja annak a hitelesítő adatnak a nevét, amit ez a parancsmag módosít.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Megadja annak az erőforráscsoportnak a nevét, amelynek a parancsmagja módosítja a hitelesítő adatait.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Érték
A hitelesítő adatokat **PSCredential** objektumként adja meg.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Management.Automation.PSCredential

## KIMENETEK

### Microsoft.Azure.Commands.Automation.Model.CredentialInfo

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzAutomationCredential](./Get-AzAutomationCredential.md)

[New-AzAutomationCredential](./New-AzAutomationCredential.md)

[Remove-AzAutomationCredential](./Remove-AzAutomationCredential.md)


