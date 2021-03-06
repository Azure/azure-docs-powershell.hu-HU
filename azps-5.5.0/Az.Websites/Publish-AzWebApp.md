---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207455"
---
# Publish-AzWebApp

## SYNOPSIS
Zip, JAR vagy WAR fájlból telepíti az Azure Web Appot zipdeploy használatával. 

## SZINTAXIS

### FromResourceName
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromWebApp
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## LEÍRÁS
A **Publish-AzWebApp** parancsmag egy meglévő Azure Web Appba tölti fel a tartalmat. A tartalmat ZIP-fájlba kell csomagolni, ha kötegeket használ (például .NET, Python vagy Node) vagy EGY WAR vagy JAR fájlt a Java használata esetén. A tartalomnak előre meg kell épülni és használatra késznek kell lennie, és nem kell további build lépéseket elrendelni a telepítés során. Ez a parancsmag a Kudu zipdeploy és a zipeploy funkciókat használja a tartalom központi telepítéséhez. A kudu wikin részletesen tájékozódhat arról, hogy miként működik a zipdeploy és a zipeploy, és hogyan lehet megfelelően csomagolni egy webalkalmazást telepítésre. https://aka.ms/kuduzipdeploy és https://aka.ms/kuduwardeploy hasznos részleteket tartalmaz a zipdeploy és a zipeploy fájlról.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

Feltölti a app.zip a Default-Web-WestUS erőforráscsoporthoz tartozó MyApp nevű webappba.

### 2. példa
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

Feltölti a javaproject.war fájl tartalmát a ContosoRg erőforráscsoporthoz tartozó ContosoApp nevű webapp átmeneti tárolóhelyre.

### 3. példa
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

Feltölti a app.zip ContosoApp nevű webappba, amely a ContosoRG erőforráscsoporthoz tartozik. A parancsmagot a háttérben futó feladat fogja futtatni.

### 4. példa
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### 5. példa
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

Feltölti a java_app.jar tartalmát a ContosoRG erőforráscsoporthoz tartozó ContosoApp nevű webappba.

## PARAMETERS

### -ArchivePath
Az archív fájl elérési útja. A ZIP, a WAR és a JAR támogatott.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Parancsmag futtatása a háttérben

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

### -Force
Forcefully Remove Option

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

### -Name
A webalkalmazás neve.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
A webalkalmazás-slot neve.

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WebApp
A webalkalmazás-objektum

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## KIMENETEK

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
