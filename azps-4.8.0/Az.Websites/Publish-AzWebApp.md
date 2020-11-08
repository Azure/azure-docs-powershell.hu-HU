---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 6080f9a5c8ceb18aa2bf6a37a034372d3bfb40a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025025"
---
# Publish-AzWebApp

## Áttekintés
Az Azure Web App telepítése ZIP-, JAR-vagy háborús fájlból a zipdeploy segítségével. 

## SZINTAXISA

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

## Leírás
A **Közzététel-AzWebApp** parancsmag a tartalmat egy meglévő Azure Web App alkalmazásba tölti fel. A tartalmat egy ZIP-fájlba kell csomagolni, ha például a .NET, a Python vagy a Node, vagy egy olyan HÁBORÚt vagy JAR fájlt használ, amely Java-ot használ. A tartalmat előre kell létrehozni, és a telepítés során további lépéseket kell elkészítenie. Ez a parancsmag a kudu zipdeploy és a wardeploy funkciókat használja a tartalom központi telepítéséhez. A kudu wikiben további információt talál arról, hogy hogyan működik a zipdeploy és a wardeploy, és hogyan lehet megfelelően becsomagolni egy webalkalmazást a központi üzembe helyezéshez. https://aka.ms/kuduzipdeploy és https://aka.ms/kuduwardeploy a zipdeploy és a wardeploy hasznos információkat tartalmaz.

## Példák

### Példa 1
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

A app.zip tartalmát feltölti a SajátPr nevű webalkalmazásba, amely az erőforráscsoport alapértelmezett verziójához tartozik – web-WestUS.

### 2. példa
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

Feltölti a javaproject. War fájl tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazás átmeneti nyílásába.

### 3. példa
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

Feltölti app.zip tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazásba. A parancsmagot a program háttérben futtatja.

### 4. példa
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### Példa 5
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

Feltölti a java_app. jar tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazásra.

## PARAMÉTEREK

### -ArchivePath
Az archív fájl elérési útvonala. A program támogatja a ZIP, a WAR és a JAR használatát.

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
A parancsmag futtatása a háttérben

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
Kényszerített eltávolítási lehetőség

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

### -Name (név)
A Web App neve.

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
A Web App-bővítőhely neve.

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
A Web App-objektum

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. WebApps. models. PSSite

## KIMENETEK

### Microsoft. Azure. Command. WebApps. models. PSSite

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
