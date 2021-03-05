---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 9a1c1de8aef41089cfc874cf35b26fcc9bf0be52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011126"
---
# <span data-ttu-id="7fffe-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fffe-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="7fffe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fffe-102">SYNOPSIS</span></span>
<span data-ttu-id="7fffe-103">Azure App Service-előfizetést hoz létre egy adott földrajzi helyen.</span><span class="sxs-lookup"><span data-stu-id="7fffe-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="7fffe-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fffe-104">SYNTAX</span></span>

### <span data-ttu-id="7fffe-105">S1</span><span class="sxs-lookup"><span data-stu-id="7fffe-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-Tag <Hashtable>] [-Linux] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fffe-106">S2</span><span class="sxs-lookup"><span data-stu-id="7fffe-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fffe-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fffe-107">DESCRIPTION</span></span>
<span data-ttu-id="7fffe-108">A **New-AzAppServicePlan** parancsmag létrehoz egy Azure App Service-tervet egy adott földrajzi helyen, a megadott szinttel, a dolgozók méretével és a dolgozók számával.</span><span class="sxs-lookup"><span data-stu-id="7fffe-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="7fffe-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fffe-109">EXAMPLES</span></span>

### <span data-ttu-id="7fffe-110">1. példa: Appszolgáltatás-csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="7fffe-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="7fffe-111">Ez a parancs létrehoz egy ContosoASP nevű appszolgáltatás-tervet a Default-Web-WestUS nevű erőforráscsoportban a Földrajzi hely nyugati részén.</span><span class="sxs-lookup"><span data-stu-id="7fffe-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="7fffe-112">A parancs egy alapszintet ad meg, és két kis dolgozót foglal ki.</span><span class="sxs-lookup"><span data-stu-id="7fffe-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="7fffe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fffe-113">PARAMETERS</span></span>

### <span data-ttu-id="7fffe-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fffe-114">-AppServicePlan</span></span>
<span data-ttu-id="7fffe-115">App Service Plan objektum</span><span class="sxs-lookup"><span data-stu-id="7fffe-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="7fffe-116">-AseName</span></span>
<span data-ttu-id="7fffe-117">Appszolgáltatás-környezet neve</span><span class="sxs-lookup"><span data-stu-id="7fffe-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fffe-118">-AseResourceGroupName</span></span>
<span data-ttu-id="7fffe-119">App Service Environment Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="7fffe-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fffe-120">-AsJob</span></span>
<span data-ttu-id="7fffe-121">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="7fffe-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fffe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fffe-122">-DefaultProfile</span></span>
<span data-ttu-id="7fffe-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fffe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fffe-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="7fffe-124">-HyperV</span></span>
<span data-ttu-id="7fffe-125">Adja meg, az App Service Plan a Windows-tárolókat fogja futtatni</span><span class="sxs-lookup"><span data-stu-id="7fffe-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-126">-Linux</span><span class="sxs-lookup"><span data-stu-id="7fffe-126">-Linux</span></span>
<span data-ttu-id="7fffe-127">Adja meg, hogy az appszolgáltatás-csomag Linux-tárolókat fog futtatni</span><span class="sxs-lookup"><span data-stu-id="7fffe-127">Specify this, App Service Plan will run Linux Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-128">-Location</span><span class="sxs-lookup"><span data-stu-id="7fffe-128">-Location</span></span>
<span data-ttu-id="7fffe-129">Hely</span><span class="sxs-lookup"><span data-stu-id="7fffe-129">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-130">-Name</span><span class="sxs-lookup"><span data-stu-id="7fffe-130">-Name</span></span>
<span data-ttu-id="7fffe-131">Appszolgáltatás-terv neve</span><span class="sxs-lookup"><span data-stu-id="7fffe-131">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-132">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="7fffe-132">-NumberofWorkers</span></span>
<span data-ttu-id="7fffe-133">Dolgozók száma</span><span class="sxs-lookup"><span data-stu-id="7fffe-133">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-134">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="7fffe-134">-PerSiteScaling</span></span>
<span data-ttu-id="7fffe-135">Engedélyezi-e a webhelyenkénti méretezést?</span><span class="sxs-lookup"><span data-stu-id="7fffe-135">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fffe-136">-ResourceGroupName</span></span>
<span data-ttu-id="7fffe-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7fffe-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="7fffe-138">-Tag</span></span>
<span data-ttu-id="7fffe-139">A címkék olyan név/érték párok, amelyek lehetővé teszik az erőforrások kategorizálását</span><span class="sxs-lookup"><span data-stu-id="7fffe-139">Tags are name/value pairs that enable you to categorize resources</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-140">-Tier</span><span class="sxs-lookup"><span data-stu-id="7fffe-140">-Tier</span></span>
<span data-ttu-id="7fffe-141">Tier</span><span class="sxs-lookup"><span data-stu-id="7fffe-141">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-142">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="7fffe-142">-WorkerSize</span></span>
<span data-ttu-id="7fffe-143">Webmunkások mérete</span><span class="sxs-lookup"><span data-stu-id="7fffe-143">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fffe-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fffe-144">CommonParameters</span></span>
<span data-ttu-id="7fffe-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fffe-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fffe-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fffe-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fffe-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fffe-147">INPUTS</span></span>

### <span data-ttu-id="7fffe-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fffe-148">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="7fffe-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fffe-149">OUTPUTS</span></span>

### <span data-ttu-id="7fffe-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fffe-150">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="7fffe-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fffe-151">NOTES</span></span>

## <span data-ttu-id="7fffe-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fffe-152">RELATED LINKS</span></span>

[<span data-ttu-id="7fffe-153">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fffe-153">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="7fffe-154">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fffe-154">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="7fffe-155">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7fffe-155">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


