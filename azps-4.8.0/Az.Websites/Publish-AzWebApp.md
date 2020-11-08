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
# <span data-ttu-id="474b2-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="474b2-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="474b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="474b2-102">SYNOPSIS</span></span>
<span data-ttu-id="474b2-103">Az Azure Web App telepítése ZIP-, JAR-vagy háborús fájlból a zipdeploy segítségével.</span><span class="sxs-lookup"><span data-stu-id="474b2-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="474b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="474b2-104">SYNTAX</span></span>

### <span data-ttu-id="474b2-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="474b2-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>]  [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="474b2-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="474b2-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-Force] [-DefaultProfile <IAzureContextContainer>] 
 [<CommonParameters>]
```

## <span data-ttu-id="474b2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="474b2-107">DESCRIPTION</span></span>
<span data-ttu-id="474b2-108">A **Közzététel-AzWebApp** parancsmag a tartalmat egy meglévő Azure Web App alkalmazásba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="474b2-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="474b2-109">A tartalmat egy ZIP-fájlba kell csomagolni, ha például a .NET, a Python vagy a Node, vagy egy olyan HÁBORÚt vagy JAR fájlt használ, amely Java-ot használ.</span><span class="sxs-lookup"><span data-stu-id="474b2-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="474b2-110">A tartalmat előre kell létrehozni, és a telepítés során további lépéseket kell elkészítenie.</span><span class="sxs-lookup"><span data-stu-id="474b2-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="474b2-111">Ez a parancsmag a kudu zipdeploy és a wardeploy funkciókat használja a tartalom központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="474b2-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="474b2-112">A kudu wikiben további információt talál arról, hogy hogyan működik a zipdeploy és a wardeploy, és hogyan lehet megfelelően becsomagolni egy webalkalmazást a központi üzembe helyezéshez.</span><span class="sxs-lookup"><span data-stu-id="474b2-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="474b2-113"> https://aka.ms/kuduzipdeploy és https://aka.ms/kuduwardeploy a zipdeploy és a wardeploy hasznos információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="474b2-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="474b2-114">Példák</span><span class="sxs-lookup"><span data-stu-id="474b2-114">EXAMPLES</span></span>

### <span data-ttu-id="474b2-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="474b2-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="474b2-116">A app.zip tartalmát feltölti a SajátPr nevű webalkalmazásba, amely az erőforráscsoport alapértelmezett verziójához tartozik – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="474b2-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="474b2-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="474b2-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="474b2-118">Feltölti a javaproject. War fájl tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazás átmeneti nyílásába.</span><span class="sxs-lookup"><span data-stu-id="474b2-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="474b2-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="474b2-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="474b2-120">Feltölti app.zip tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="474b2-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="474b2-121">A parancsmagot a program háttérben futtatja.</span><span class="sxs-lookup"><span data-stu-id="474b2-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="474b2-122">4. példa</span><span class="sxs-lookup"><span data-stu-id="474b2-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```
### <span data-ttu-id="474b2-123">Példa 5</span><span class="sxs-lookup"><span data-stu-id="474b2-123">Example 5</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -Force
```

<span data-ttu-id="474b2-124">Feltölti a java_app. jar tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="474b2-124">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="474b2-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="474b2-125">PARAMETERS</span></span>

### <span data-ttu-id="474b2-126">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="474b2-126">-ArchivePath</span></span>
<span data-ttu-id="474b2-127">Az archív fájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="474b2-127">The path of the archive file.</span></span> <span data-ttu-id="474b2-128">A program támogatja a ZIP, a WAR és a JAR használatát.</span><span class="sxs-lookup"><span data-stu-id="474b2-128">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="474b2-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="474b2-129">-AsJob</span></span>
<span data-ttu-id="474b2-130">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="474b2-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="474b2-131">-Force</span><span class="sxs-lookup"><span data-stu-id="474b2-131">-Force</span></span>
<span data-ttu-id="474b2-132">Kényszerített eltávolítási lehetőség</span><span class="sxs-lookup"><span data-stu-id="474b2-132">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="474b2-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474b2-133">-DefaultProfile</span></span>
<span data-ttu-id="474b2-134">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="474b2-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="474b2-135">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="474b2-135">-Name</span></span>
<span data-ttu-id="474b2-136">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="474b2-136">The name of the web app.</span></span>

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

### <span data-ttu-id="474b2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474b2-137">-ResourceGroupName</span></span>
<span data-ttu-id="474b2-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="474b2-138">The name of the resource group.</span></span>

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

### <span data-ttu-id="474b2-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="474b2-139">-Slot</span></span>
<span data-ttu-id="474b2-140">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="474b2-140">The name of the web app slot.</span></span>

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

### <span data-ttu-id="474b2-141">-WebApp</span><span class="sxs-lookup"><span data-stu-id="474b2-141">-WebApp</span></span>
<span data-ttu-id="474b2-142">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="474b2-142">The web app object</span></span>

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

### <span data-ttu-id="474b2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474b2-143">CommonParameters</span></span>
<span data-ttu-id="474b2-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="474b2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474b2-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474b2-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474b2-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="474b2-146">INPUTS</span></span>

### <span data-ttu-id="474b2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="474b2-147">System.String</span></span>

### <span data-ttu-id="474b2-148">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="474b2-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="474b2-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="474b2-149">OUTPUTS</span></span>

### <span data-ttu-id="474b2-150">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="474b2-150">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="474b2-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="474b2-151">NOTES</span></span>

## <span data-ttu-id="474b2-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="474b2-152">RELATED LINKS</span></span>
