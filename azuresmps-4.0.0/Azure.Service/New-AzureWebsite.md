---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110478"
---
# New-AzureWebsite

## SYNOPSIS
Hozzon létre egy új webhelyet az Azure-ban való futtatáshoz.

## SZINTAXIS

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## LEÍRÁS
Ez a témakör a Microsoft Azure PowerShell modul 0.8.10-es verziójában található parancsmagot ismerteti.
A használt modul verziójának lekérte az Azure PowerShell konzolban a `(Get-Module -Name Azure).Version` következőt: .

A parancsmag létrehoz egy új webhelyet az Azure-ban való futtatáshoz, és felkészül a GitHubon keresztüli telepítésre.

## PÉLDÁK

### 1. példa: Új webhely létrehozása a Git segítségével
```
PS C:\> New-AzureWebsite mySite -Git
```

Ebben a példában egy új webhelyet hoz létre az Azure-ban, és egy helyi Git-tárházat, használhatja a fájlok új webhelyre való telepítéséhez.

### 2. példa: Webhely létrehozása a GitHubbal integrálva
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

Ez a példa létrehoz egy új webhelyet, amely egy Myaccount/myrepo nevű GitHub-tárházhoz van csatolva.
A GitHub-tárházba való kötelezettséget a rendszer az Azure-ban a webhelyre tetszetzi.

## PARAMETERS

### -Git
Beállítja a helyi Git-tárat, és a webhelyre mutató hivatkozást hoz létre.
Ha meg van adva, ez a paraméter beállítja a Git-tárat a helyi címtárban, és hozzáad egy "azure" nevű távoli tárat, amely az Azure-beli webhelyre mutató hivatkozást tartalmaz.

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
Azt jelzi, hogy ez a parancsmag egy meglévő GitHub-tárházhoz kapcsolódik az új webhelyhez.
A Giuthub-tárházba való kötelezettséget a rendszer az Azure-ban a webhelyre tolta.

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

### -GitHubCredentials
A GitHubhoz való csatlakozáshoz használt felhasználónév és jelszó hitelesítő adatait adja meg.

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

### -GitHubRepository
A webhelyre mutató hivatkozás gitHub-tár teljes nevét adja meg.
`myaccount/myrepo`Például.

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

### -Hostname
Az új webhely alternatív állomásnevét adja meg.

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

### -Location
Megadja annak az adatközpontnak a helyét, ahová a webhelyet telepíteni szeretné.

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

### -Name
Megadja a webhely nevét.

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
Azt az Azure-profilt adja meg, amelyből a parancsmag olvas.
Ha nem ad meg profilt, ez a parancsmag a helyi alapértelmezett profilból olvassa be.

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
Az Azure Portal for Git-telepítésben megadott felhasználónevet adja meg.

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
Megadja a webhely helynevét.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

## KIMENETEK

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Set-AzureWebsite](./Set-AzureWebsite.md)


