---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 726f991f5e51b6196b61a6e977ba1c5d4a1debf0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014454"
---
# <span data-ttu-id="f87c7-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f87c7-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="f87c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f87c7-102">SYNOPSIS</span></span>
<span data-ttu-id="f87c7-103">Zip, JAR vagy WAR fájlból telepíti az Azure Web Appot zipdeploy használatával.</span><span class="sxs-lookup"><span data-stu-id="f87c7-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="f87c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f87c7-104">SYNTAX</span></span>

### <span data-ttu-id="f87c7-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f87c7-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f87c7-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f87c7-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="f87c7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f87c7-107">DESCRIPTION</span></span>
<span data-ttu-id="f87c7-108">A **Publish-AzWebApp** parancsmag tartalmat tölt fel egy meglévő Azure Web Appba.</span><span class="sxs-lookup"><span data-stu-id="f87c7-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="f87c7-109">A tartalmat ZIP-fájlba kell csomagolni, ha kötegeket használ (például .NET, Python vagy Node) vagy EGY WAR vagy JAR fájlt a Java használata esetén.</span><span class="sxs-lookup"><span data-stu-id="f87c7-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="f87c7-110">A tartalomnak előre beépítettnek és használatra késznek kell lennie, további build lépések nélkül a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="f87c7-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="f87c7-111">Ez a parancsmag a Kudu zipdeploy és a zipeploy funkciókat használja a tartalom központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="f87c7-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="f87c7-112">A kudu wikin részletesen tájékozódhat arról, hogy miként működik a zipdeploy és a zipeploy, és hogyan lehet megfelelően csomagolni egy webalkalmazást telepítésre.</span><span class="sxs-lookup"><span data-stu-id="f87c7-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="f87c7-113"> https://aka.ms/kuduzipdeploy és https://aka.ms/kuduwardeploy hasznos részleteket tartalmaz a zipdeploy és a zipeploy fájlról.</span><span class="sxs-lookup"><span data-stu-id="f87c7-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="f87c7-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f87c7-114">EXAMPLES</span></span>

### <span data-ttu-id="f87c7-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="f87c7-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="f87c7-116">Feltölti a app.zip a Default-Web-WestUS erőforráscsoporthoz tartozó MyApp nevű webappba.</span><span class="sxs-lookup"><span data-stu-id="f87c7-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="f87c7-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="f87c7-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="f87c7-118">Feltölti a javaproject.war fájl tartalmát a ContosoRg erőforráscsoporthoz tartozó ContosoApp nevű webapp átmeneti tárolóhelyre.</span><span class="sxs-lookup"><span data-stu-id="f87c7-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="f87c7-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="f87c7-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="f87c7-120">Feltölti a app.zip ContosoApp nevű webappba, amely a ContosoRG erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="f87c7-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="f87c7-121">A parancsmagot a háttérben futó feladat fogja futtatni.</span><span class="sxs-lookup"><span data-stu-id="f87c7-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="f87c7-122">4. példa</span><span class="sxs-lookup"><span data-stu-id="f87c7-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="f87c7-123">5. példa</span><span class="sxs-lookup"><span data-stu-id="f87c7-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="f87c7-124">Feltölti a java_app.jar tartalmát a ContosoRG erőforráscsoporthoz tartozó ContosoApp nevű webappba.</span><span class="sxs-lookup"><span data-stu-id="f87c7-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="f87c7-125">6. példa</span><span class="sxs-lookup"><span data-stu-id="f87c7-125">Example 6</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Timeout 300000 -Force
```

<span data-ttu-id="f87c7-126">Feltölti a java_app.jar tartalmát a ContosoRG erőforráscsoporthoz tartozó ContosoApp nevű webappba.</span><span class="sxs-lookup"><span data-stu-id="f87c7-126">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="f87c7-127">A felhasználó ezredmásodpercben meg tudja várni a kérés időkorrekét.</span><span class="sxs-lookup"><span data-stu-id="f87c7-127">User can Sets the timespan in Milliseconds to wait before the request times out.</span></span>

## <span data-ttu-id="f87c7-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f87c7-128">PARAMETERS</span></span>

### <span data-ttu-id="f87c7-129">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="f87c7-129">-ArchivePath</span></span>
<span data-ttu-id="f87c7-130">Az archív fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="f87c7-130">The path of the archive file.</span></span> <span data-ttu-id="f87c7-131">A ZIP, a WAR és a JAR támogatott.</span><span class="sxs-lookup"><span data-stu-id="f87c7-131">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="f87c7-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f87c7-132">-AsJob</span></span>
<span data-ttu-id="f87c7-133">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f87c7-133">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f87c7-134">-Force</span><span class="sxs-lookup"><span data-stu-id="f87c7-134">-Force</span></span>
<span data-ttu-id="f87c7-135">Forcefully Remove Option</span><span class="sxs-lookup"><span data-stu-id="f87c7-135">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="f87c7-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87c7-136">-DefaultProfile</span></span>
<span data-ttu-id="f87c7-137">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f87c7-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f87c7-138">-Name</span><span class="sxs-lookup"><span data-stu-id="f87c7-138">-Name</span></span>
<span data-ttu-id="f87c7-139">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="f87c7-139">The name of the web app.</span></span>

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

### <span data-ttu-id="f87c7-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f87c7-140">-ResourceGroupName</span></span>
<span data-ttu-id="f87c7-141">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f87c7-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="f87c7-142">-Slot</span><span class="sxs-lookup"><span data-stu-id="f87c7-142">-Slot</span></span>
<span data-ttu-id="f87c7-143">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="f87c7-143">The name of the web app slot.</span></span>

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

### <span data-ttu-id="f87c7-144">-Timeout</span><span class="sxs-lookup"><span data-stu-id="f87c7-144">-Timeout</span></span>
<span data-ttu-id="f87c7-145">Ezredmásodpercben beállítja, hogy a kérelem időkorrekta előtt ezredmásodpercben várjon.</span><span class="sxs-lookup"><span data-stu-id="f87c7-145">Sets the timespan in Milliseconds to wait before the request times out.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87c7-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f87c7-146">-WebApp</span></span>
<span data-ttu-id="f87c7-147">A webalkalmazás-objektum</span><span class="sxs-lookup"><span data-stu-id="f87c7-147">The web app object</span></span>

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

### <span data-ttu-id="f87c7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87c7-148">CommonParameters</span></span>
<span data-ttu-id="f87c7-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87c7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87c7-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f87c7-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87c7-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f87c7-151">INPUTS</span></span>

### <span data-ttu-id="f87c7-152">System.String</span><span class="sxs-lookup"><span data-stu-id="f87c7-152">System.String</span></span>

### <span data-ttu-id="f87c7-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f87c7-153">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f87c7-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f87c7-154">OUTPUTS</span></span>

### <span data-ttu-id="f87c7-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f87c7-155">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f87c7-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f87c7-156">NOTES</span></span>

## <span data-ttu-id="f87c7-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f87c7-157">RELATED LINKS</span></span>
