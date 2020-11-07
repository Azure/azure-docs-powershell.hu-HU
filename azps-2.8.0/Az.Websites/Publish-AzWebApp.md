---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/publish-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Publish-AzWebApp.md
ms.openlocfilehash: 07ec4223414bbdbab8e3fa4d11641d040d918209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839862"
---
# <span data-ttu-id="1100e-101">Publish-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1100e-101">Publish-AzWebApp</span></span>

## <span data-ttu-id="1100e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1100e-102">SYNOPSIS</span></span>
<span data-ttu-id="1100e-103">Az Azure Web App telepítése ZIP-, JAR-vagy háborús fájlból a zipdeploy segítségével.</span><span class="sxs-lookup"><span data-stu-id="1100e-103">Deploys an Azure Web App from a ZIP, JAR, or WAR file using zipdeploy.</span></span> 

## <span data-ttu-id="1100e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1100e-104">SYNTAX</span></span>

### <span data-ttu-id="1100e-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1100e-105">FromResourceName</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1100e-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1100e-106">FromWebApp</span></span>
```
Publish-AzWebApp -ArchivePath <String> [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1100e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1100e-107">DESCRIPTION</span></span>
<span data-ttu-id="1100e-108">A **Közzététel-AzWebApp** parancsmag a tartalmat egy meglévő Azure Web App alkalmazásba tölti fel.</span><span class="sxs-lookup"><span data-stu-id="1100e-108">The **Publish-AzWebApp** cmdlet uploads content to an existing Azure Web App.</span></span> <span data-ttu-id="1100e-109">A tartalmat egy ZIP-fájlba kell csomagolni, ha például a .NET, a Python vagy a Node, vagy egy olyan HÁBORÚt vagy JAR fájlt használ, amely Java-ot használ.</span><span class="sxs-lookup"><span data-stu-id="1100e-109">The content should be packaged in a ZIP file if using stacks such as .NET, Python, or Node, or a WAR or JAR file if using Java.</span></span> <span data-ttu-id="1100e-110">A tartalmat előre kell létrehozni, és a telepítés során további lépéseket kell elkészítenie.</span><span class="sxs-lookup"><span data-stu-id="1100e-110">The content should be pre-built and ready-to-run without any additional build steps during deployment.</span></span> <span data-ttu-id="1100e-111">Ez a parancsmag a kudu zipdeploy és a wardeploy funkciókat használja a tartalom központi telepítéséhez.</span><span class="sxs-lookup"><span data-stu-id="1100e-111">This cmdlet uses the Kudu zipdeploy and wardeploy features to deploy content.</span></span> <span data-ttu-id="1100e-112">A kudu wikiben további információt talál arról, hogy hogyan működik a zipdeploy és a wardeploy, és hogyan lehet megfelelően becsomagolni egy webalkalmazást a központi üzembe helyezéshez.</span><span class="sxs-lookup"><span data-stu-id="1100e-112">Refer to the Kudu wiki for details about how zipdeploy and wardeploy work, and how to properly package a web app for deployment.</span></span> <span data-ttu-id="1100e-113"> https://aka.ms/kuduzipdeploy és https://aka.ms/kuduwardeploy a zipdeploy és a wardeploy hasznos információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="1100e-113">https://aka.ms/kuduzipdeploy and https://aka.ms/kuduwardeploy contain helpful details about zipdeploy and wardeploy.</span></span>

## <span data-ttu-id="1100e-114">Példák</span><span class="sxs-lookup"><span data-stu-id="1100e-114">EXAMPLES</span></span>

### <span data-ttu-id="1100e-115">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1100e-115">Example 1</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName Default-Web-WestUS -Name MyApp -ArchivePath C:\project\app.zip
```

<span data-ttu-id="1100e-116">A app.zip tartalmát feltölti a SajátPr nevű webalkalmazásba, amely az erőforráscsoport alapértelmezett verziójához tartozik – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1100e-116">Uploads the contents of app.zip to the web app named MyApp belonging to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="1100e-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="1100e-117">Example 2</span></span>
```powershell
PS C:\> Publish-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp -Slot Staging -ArchivePath C:\project\javaproject.war
```

<span data-ttu-id="1100e-118">Feltölti a javaproject. War fájl tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazás átmeneti nyílásába.</span><span class="sxs-lookup"><span data-stu-id="1100e-118">Uploads the contents of javaproject.war to the Staging slot of the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

### <span data-ttu-id="1100e-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="1100e-119">Example 3</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> Publish-AzWebApp -WebApp $app -ArchivePath C:\project\app.zip -AsJob
```

<span data-ttu-id="1100e-120">Feltölti app.zip tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazásba.</span><span class="sxs-lookup"><span data-stu-id="1100e-120">Uploads the contents of app.zip to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span> <span data-ttu-id="1100e-121">A parancsmagot a program háttérben futtatja.</span><span class="sxs-lookup"><span data-stu-id="1100e-121">The cmdlet will be run in a background job.</span></span>

### <span data-ttu-id="1100e-122">4. példa</span><span class="sxs-lookup"><span data-stu-id="1100e-122">Example 4</span></span>
```powershell
PS C:\> $app = Get-AzWebApp -ResourceGroupName ContosoRG -Name ContosoApp
PS C:\> $app | Publish-AzWebApp -ArchivePath C:\project\java_app.jar
```

<span data-ttu-id="1100e-123">Feltölti a java_app. jar tartalmát az erőforráscsoport ContosoRG tartozó ContosoApp nevű webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="1100e-123">Uploads the contents of java_app.jar to the web app named ContosoApp belonging to the resource group ContosoRG.</span></span>

## <span data-ttu-id="1100e-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1100e-124">PARAMETERS</span></span>

### <span data-ttu-id="1100e-125">-ArchivePath</span><span class="sxs-lookup"><span data-stu-id="1100e-125">-ArchivePath</span></span>
<span data-ttu-id="1100e-126">Az archív fájl elérési útvonala.</span><span class="sxs-lookup"><span data-stu-id="1100e-126">The path of the archive file.</span></span> <span data-ttu-id="1100e-127">A program támogatja a ZIP, a WAR és a JAR használatát.</span><span class="sxs-lookup"><span data-stu-id="1100e-127">ZIP, WAR, and JAR are supported.</span></span>

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

### <span data-ttu-id="1100e-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1100e-128">-AsJob</span></span>
<span data-ttu-id="1100e-129">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1100e-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1100e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1100e-130">-DefaultProfile</span></span>
<span data-ttu-id="1100e-131">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1100e-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1100e-132">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1100e-132">-Name</span></span>
<span data-ttu-id="1100e-133">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="1100e-133">The name of the web app.</span></span>

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

### <span data-ttu-id="1100e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1100e-134">-ResourceGroupName</span></span>
<span data-ttu-id="1100e-135">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1100e-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="1100e-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="1100e-136">-Slot</span></span>
<span data-ttu-id="1100e-137">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="1100e-137">The name of the web app slot.</span></span>

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

### <span data-ttu-id="1100e-138">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1100e-138">-WebApp</span></span>
<span data-ttu-id="1100e-139">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="1100e-139">The web app object</span></span>

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

### <span data-ttu-id="1100e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1100e-140">CommonParameters</span></span>
<span data-ttu-id="1100e-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1100e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1100e-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1100e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1100e-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1100e-143">INPUTS</span></span>

### <span data-ttu-id="1100e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="1100e-144">System.String</span></span>

### <span data-ttu-id="1100e-145">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1100e-145">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1100e-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1100e-146">OUTPUTS</span></span>

### <span data-ttu-id="1100e-147">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="1100e-147">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1100e-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1100e-148">NOTES</span></span>

## <span data-ttu-id="1100e-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1100e-149">RELATED LINKS</span></span>
