---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015831"
---
# Set-AzureAutomationCredential

## Áttekintés

A hitelesítő adatok módosítása az automatizálásban.

## SZINTAXISA

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

A **set-AzureAutomationCredential** parancsmag **PSCredential** -objektumként módosítja a hitelesítő adatokat a Microsoft Azure automatizálási szolgáltatásban.

## Példák

### Példa 1: hitelesítő adatok frissítése
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

Ezek a parancsok frissítik a MyCredential nevű meglévő hitelesítő adatokat.
Először létrejön egy hitelesítőadat-objektum, amely tartalmazza a felhasználónevet és a jelszót.
Ezt követően a rendszer az utolsó parancsban használja az automatizálási hitelesítő adatok frissítését.

## PARAMÉTEREK

### -AutomationAccountName
A hitelesítő adatokkal rendelkező automatizálási fiók nevét adja meg.

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

### -Leírás
A hitelesítő adatok leírását adja meg.

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

### -Name (név)
A hitelesítő adatok nevét adja meg.

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

### -Value (érték)
A hitelesítő adatokat **PSCredential** -objektumként adja meg.

```yaml
Type: PSCredential
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

## KIMENETEK

### Microsoft. Azure. Command. Automation. Model. CredentialInfo

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureAutomationCredential](./Get-AzureAutomationCredential.md)

[Új – AzureAutomationCredential](./New-AzureAutomationCredential.md)

[Remove-AzureAutomationCredential](./Remove-AzureAutomationCredential.md)


