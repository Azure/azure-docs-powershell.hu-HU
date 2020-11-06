---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09300c7d7d8394dbcfed36560c988f0193473c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491825"
---
# <span data-ttu-id="5b467-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5b467-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="5b467-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b467-102">SYNOPSIS</span></span>
<span data-ttu-id="5b467-103">Azure app-szolgáltatási csomagot hoz létre egy adott földrajzi helyen.</span><span class="sxs-lookup"><span data-stu-id="5b467-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b467-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b467-104">SYNTAX</span></span>

### <span data-ttu-id="5b467-105">S1</span><span class="sxs-lookup"><span data-stu-id="5b467-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b467-106">S2</span><span class="sxs-lookup"><span data-stu-id="5b467-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b467-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b467-107">DESCRIPTION</span></span>
<span data-ttu-id="5b467-108">A **New-AzureRmAppServicePlan** parancsmag létrehoz egy Azure app-szolgáltatási csomagot egy adott földrajzi helyen, a megadott szinttel, a munkás méretével és a munkavállalók számával.</span><span class="sxs-lookup"><span data-stu-id="5b467-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="5b467-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5b467-109">EXAMPLES</span></span>

### <span data-ttu-id="5b467-110">1. példa: alkalmazás-szolgáltatási csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="5b467-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="5b467-111">Ez a parancs létrehoz egy ContosoASP nevű app-szolgáltatási csomagot a Default-Web-WestUS földrajzi helyének West US nevű erőforráscsoport nevű erőforráscsoport nevű csoportjában.</span><span class="sxs-lookup"><span data-stu-id="5b467-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="5b467-112">A parancs egy alapszintet határoz meg, és két kisméretű dolgozót oszt szét.</span><span class="sxs-lookup"><span data-stu-id="5b467-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="5b467-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b467-113">PARAMETERS</span></span>

### <span data-ttu-id="5b467-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5b467-114">-AppServicePlan</span></span>
<span data-ttu-id="5b467-115">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="5b467-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="5b467-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="5b467-116">-AseName</span></span>
<span data-ttu-id="5b467-117">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="5b467-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="5b467-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b467-118">-AseResourceGroupName</span></span>
<span data-ttu-id="5b467-119">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="5b467-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="5b467-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b467-120">-AsJob</span></span>
<span data-ttu-id="5b467-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5b467-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b467-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b467-122">-DefaultProfile</span></span>
<span data-ttu-id="5b467-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b467-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b467-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="5b467-124">-HyperV</span></span>
<span data-ttu-id="5b467-125">Adja meg ezt az alkalmazást, és a Windows-tárolókat fogja futtatni.</span><span class="sxs-lookup"><span data-stu-id="5b467-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="5b467-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="5b467-126">-Location</span></span>
<span data-ttu-id="5b467-127">Helyre</span><span class="sxs-lookup"><span data-stu-id="5b467-127">Location</span></span> 

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

### <span data-ttu-id="5b467-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b467-128">-Name</span></span>
<span data-ttu-id="5b467-129">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="5b467-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="5b467-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="5b467-130">-NumberofWorkers</span></span>
<span data-ttu-id="5b467-131">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="5b467-131">Number Of Workers</span></span>

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

### <span data-ttu-id="5b467-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="5b467-132">-PerSiteScaling</span></span>
<span data-ttu-id="5b467-133">A webhelyek méretezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5b467-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="5b467-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b467-134">-ResourceGroupName</span></span>
<span data-ttu-id="5b467-135">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5b467-135">Resource Group Name</span></span>

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

### <span data-ttu-id="5b467-136">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="5b467-136">-Tier</span></span>
<span data-ttu-id="5b467-137">Tier</span><span class="sxs-lookup"><span data-stu-id="5b467-137">Tier</span></span>

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

### <span data-ttu-id="5b467-138">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="5b467-138">-WorkerSize</span></span>
<span data-ttu-id="5b467-139">Webes munkatárs mérete</span><span class="sxs-lookup"><span data-stu-id="5b467-139">Size of web worker</span></span>

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

### <span data-ttu-id="5b467-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b467-140">CommonParameters</span></span>
<span data-ttu-id="5b467-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b467-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b467-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b467-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b467-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b467-143">INPUTS</span></span>

### <span data-ttu-id="5b467-144">Microsoft. Azure. Management. WebSites. models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5b467-144">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="5b467-145">Paraméterek: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5b467-145">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="5b467-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b467-146">OUTPUTS</span></span>

### <span data-ttu-id="5b467-147">Microsoft. Azure. Management. WebSites. models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5b467-147">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="5b467-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b467-148">NOTES</span></span>

## <span data-ttu-id="5b467-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b467-149">RELATED LINKS</span></span>

[<span data-ttu-id="5b467-150">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5b467-150">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="5b467-151">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5b467-151">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="5b467-152">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5b467-152">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


