---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: a05662917d7e29f090867b0c91503292a9bc917e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492884"
---
# Set-AzureRmAutomationCredential

## Áttekintés
Automatizálási hitelesítő adatok módosítása

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmAutomationCredential** parancsmag **PSCredential** -objektumként módosítja a hitelesítő adatokat az Azure automatizálásban.

## Példák

### Példa 1: hitelesítő adatok frissítése
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

Az első parancs a felhasználónevet hozzárendeli a $User változóhoz.
A második parancs az egyszerű szöveges jelszót egy biztonságos karakterláncba konvertálja a ConvertTo-SecureString parancsmag használatával.
A parancs az objektumot a $Password változóban tárolja.
A harmadik parancs a hitelesítő adatokat $User és a $Password alapján hozza létre, majd a $Credential változóban tárolja.
A végleges parancs módosítja a ContosoCredential nevű automatizálási hitelesítő adatokat, hogy a hitelesítő adatokat használja a $Credentialban.

## PARAMÉTEREK

### -AutomationAccountName
Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag módosítja a hitelesítő adatokat.

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
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Leírás
A parancsmag által módosított hitelesítő adatok leírását adja meg.

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

### -Name (név)
Annak a hitelesítő adatoknak a neve, amelyet a parancsmag módosított.

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
Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez ez a parancsmag módosítja a hitelesítő adatokat.

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

### -Value (érték)
A hitelesítő adatokat **PSCredential** -objektumként adja meg.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### System. Management. Automation. PSCredential

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. CredentialInfo

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmAutomationCredential](./Get-AzureRMAutomationCredential.md)

[Új – AzureRmAutomationCredential](./New-AzureRMAutomationCredential.md)

[Remove-AzureRmAutomationCredential](./Remove-AzureRMAutomationCredential.md)


