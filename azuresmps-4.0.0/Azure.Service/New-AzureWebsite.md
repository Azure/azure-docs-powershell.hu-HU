---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016184"
---
# New-AzureWebsite

## Áttekintés
Az Azure-ban futtatandó új webhely létrehozása

## SZINTAXISA

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.
A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .

A parancsmag létrehoz egy új webhelyet az Azure-ban, és előkészíti a bevezetést a githubon keresztül.

## Példák

### Példa 1: új webhely létrehozása git segítségével
```
PS C:\> New-AzureWebsite mySite -Git
```

Ez a példa létrehoz egy új webhelyet az Azure-ban, és egy helyi git tárházat használ a fájlok új webhelyre történő központi telepítéséhez.

### 2. példa: a GitHub által integrált webhely létrehozása
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

Ez a példa létrehoz egy új webhelyet, amely a MyAccount/myrepo GitHub nevű tárházához van társítva.
Kötelezettséget vállal a GitHub repositoryra az Azure-beli webhelyre.

## PARAMÉTEREK

### -Git
Egy helyi git repositoryt hoz létre, és a webhelyre hivatkozik.
Ha meg van adva, ez a paraméter egy git-tárházat hoz létre a helyi címtárban, és felvesz egy "Azure" nevű távoli tárházat, amely az Azure webhelyére mutató hivatkozásokat tartalmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHub
Jelzi, hogy ez a parancsmag az új webhelyet egy meglévő GitHub-tárházhoz csatolja.
A Giuthub repository véglegesítése az Azure webhelyére kerül.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GithubCredentials
A Felhasználónév és a jelszó hitelesítő adatait adja meg a Githubhoz való csatlakozáshoz.

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

### -GithubRepository
Itt adhatja meg a webhelyre mutató GitHub-tárház teljes nevét.
Például: `myaccount/myrepo` .

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

### -Hostname (állomásnév)
Az új webhely másodlagos állomásnevét adja meg.

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

### -Hely
Annak az adatközpontnak a helyét adja meg, ahol a webhelyet telepíteni szeretné.

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
A webhely nevét adja meg.

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

### -PublishingUsername
Megadja, hogy milyen Felhasználónév van megadva az Azure portálon a git telepítéséhez.

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

### -Slot
A webhely tárolóhelyének a nevét adja meg.

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

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureWebsite](./Set-AzureWebsite.md)


