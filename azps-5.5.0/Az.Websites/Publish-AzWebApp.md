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
# <span data-ttu-id="de1b9-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="de1b9-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="de1b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="de1b9-103">Zip, JAR vagy WAR fájlból telepíti az Azure Web Appot zipdeploy használatával.</span><span class="sxs-lookup"><span data-stu-id="de1b9-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="de1b9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="de1b9-104">SYNTAX</span></span>

### <span data-ttu-id="de1b9-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="de1b9-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de1b9-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="de1b9-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="de1b9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="de1b9-107">DESCRIPTION</span></span>
<span data-ttu-id="de1b9-108">A **Publish-AzWebApp** parancsmag egy meglévő Azure Web Appba tölti fel a tartalmat.</span><span class="sxs-lookup"><span data-stu-id="de1b9-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="de1b9-109">A tartalmat ZIP-fájlba kell csomagolni, ha kötegeket használ (például .NET, Python vagy Node) vagy EGY WAR vagy JAR fájlt a Java használata esetén.</span><span class="sxs-lookup"><span data-stu-id="de1b9-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="de1b9-110">A tartalomnak előre meg kell épülni és használatra késznek kell lennie, és nem kell további build lépéseket elrendelni a telepítés során.</span><span class="sxs-lookup"><span data-stu-id="de1b9-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="de1b9-111">Ez a parancsmag a Kudu zipdeploy és a zipeploy funkciókat használja a tartalom központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="de1b9-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="de1b9-112">A kudu wikin részletesen tájékozódhat arról, hogy miként működik a zipdeploy és a zipeploy, és hogyan lehet megfelelően csomagolni egy webalkalmazást telepítésre.</span><span class="sxs-lookup"><span data-stu-id="de1b9-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="de1b9-113"> https://aka.ms/kuduzipdeploy és https://aka.ms/kuduwardeploy hasznos részleteket tartalmaz a zipdeploy és a zipeploy fájlról.</span><span class="sxs-lookup"><span data-stu-id="de1b9-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="de1b9-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="de1b9-114">EXAMPLES</span></span>

### <span data-ttu-id="de1b9-115">1. példa</span><span class="sxs-lookup"><span data-stu-id="de1b9-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="de1b9-116">Feltölti a app.zip a Default-Web-WestUS erőforráscsoporthoz tartozó MyApp nevű webappba.</span><span class="sxs-lookup"><span data-stu-id="de1b9-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="de1b9-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="de1b9-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="de1b9-118">Feltölti a javaproject.war fájl tartalmát a ContosoRg erőforráscsoporthoz tartozó ContosoApp nevű webapp átmeneti tárolóhelyre.</span><span class="sxs-lookup"><span data-stu-id="de1b9-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="de1b9-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="de1b9-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="de1b9-120">Feltölti a app.zip ContosoApp nevű webappba, amely a ContosoRG erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="de1b9-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="de1b9-121">A parancsmagot a háttérben futó feladat fogja futtatni.</span><span class="sxs-lookup"><span data-stu-id="de1b9-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="de1b9-122">4. példa</span><span class="sxs-lookup"><span data-stu-id="de1b9-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="de1b9-123">5. példa</span><span class="sxs-lookup"><span data-stu-id="de1b9-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="de1b9-124">Feltölti a java_app.jar tartalmát a ContosoRG erőforráscsoporthoz tartozó ContosoApp nevű webappba.</span><span class="sxs-lookup"><span data-stu-id="de1b9-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="de1b9-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de1b9-125">PARAMETERS</span></span>

### <span data-ttu-id="de1b9-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="de1b9-126">-ArchivePath</span></span>
<span data-ttu-id="de1b9-127">Az archív fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="de1b9-127">The path of the archive file.</span></span> <span data-ttu-id="de1b9-128">A ZIP, a WAR és a JAR támogatott.</span><span class="sxs-lookup"><span data-stu-id="de1b9-128">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="de1b9-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de1b9-129">-AsJob</span></span>
<span data-ttu-id="de1b9-130">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="de1b9-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de1b9-131">-Force</span><span class="sxs-lookup"><span data-stu-id="de1b9-131">-Force</span></span>
<span data-ttu-id="de1b9-132">Forcefully Remove Option</span><span class="sxs-lookup"><span data-stu-id="de1b9-132">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="de1b9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1b9-133">-DefaultProfile</span></span>
<span data-ttu-id="de1b9-134">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de1b9-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de1b9-135">-Name</span><span class="sxs-lookup"><span data-stu-id="de1b9-135">-Name</span></span>
<span data-ttu-id="de1b9-136">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="de1b9-136">The name of the web app.</span></span>

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

### <span data-ttu-id="de1b9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de1b9-137">-ResourceGroupName</span></span>
<span data-ttu-id="de1b9-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="de1b9-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="de1b9-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="de1b9-139">-Slot</span></span>
<span data-ttu-id="de1b9-140">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="de1b9-140">The name of the web app slot.</span></span>

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

### <span data-ttu-id="de1b9-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="de1b9-141">-WebApp</span></span>
<span data-ttu-id="de1b9-142">A webalkalmazás-objektum</span><span class="sxs-lookup"><span data-stu-id="de1b9-142">The web app object</span></span>

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

### <span data-ttu-id="de1b9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1b9-143">CommonParameters</span></span>
<span data-ttu-id="de1b9-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1b9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1b9-145">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de1b9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1b9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de1b9-146">INPUTS</span></span>

### <span data-ttu-id="de1b9-147">System.String</span><span class="sxs-lookup"><span data-stu-id="de1b9-147">System.String</span></span>

### <span data-ttu-id="de1b9-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="de1b9-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de1b9-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de1b9-149">OUTPUTS</span></span>

### <span data-ttu-id="de1b9-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="de1b9-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de1b9-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="de1b9-151">NOTES</span></span>

## <span data-ttu-id="de1b9-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de1b9-152">RELATED LINKS</span></span>
