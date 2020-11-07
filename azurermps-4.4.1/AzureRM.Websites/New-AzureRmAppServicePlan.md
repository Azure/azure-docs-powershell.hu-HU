---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: e03e7dee6e233934216c04a44c1e100d3e26347b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680211"
---
# <span data-ttu-id="9dba5-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9dba5-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="9dba5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dba5-102">SYNOPSIS</span></span>
<span data-ttu-id="9dba5-103">Azure app-szolgáltatási csomagot hoz létre egy adott földrajzi helyen.</span><span class="sxs-lookup"><span data-stu-id="9dba5-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dba5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dba5-104">SYNTAX</span></span>

### <span data-ttu-id="9dba5-105">S1</span><span class="sxs-lookup"><span data-stu-id="9dba5-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dba5-106">S2</span><span class="sxs-lookup"><span data-stu-id="9dba5-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dba5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dba5-107">DESCRIPTION</span></span>
<span data-ttu-id="9dba5-108">A **New-AzureRmAppServicePlan** parancsmag létrehoz egy Azure app-szolgáltatási csomagot egy adott földrajzi helyen, a megadott szinttel, a munkás méretével és a munkavállalók számával.</span><span class="sxs-lookup"><span data-stu-id="9dba5-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="9dba5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9dba5-109">EXAMPLES</span></span>

### <span data-ttu-id="9dba5-110">1. példa: alkalmazás-szolgáltatási csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="9dba5-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="9dba5-111">Ez a parancs létrehoz egy ContosoASP nevű app-szolgáltatási csomagot a Default-Web-WestUS földrajzi helyének West US nevű erőforráscsoport nevű erőforráscsoport nevű csoportjában.</span><span class="sxs-lookup"><span data-stu-id="9dba5-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="9dba5-112">A parancs egy alapszintet határoz meg, és két kisméretű dolgozót oszt szét.</span><span class="sxs-lookup"><span data-stu-id="9dba5-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="9dba5-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dba5-113">PARAMETERS</span></span>

### <span data-ttu-id="9dba5-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9dba5-114">-AppServicePlan</span></span>
<span data-ttu-id="9dba5-115">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="9dba5-115">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dba5-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="9dba5-116">-AseName</span></span>
<span data-ttu-id="9dba5-117">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="9dba5-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="9dba5-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dba5-118">-AseResourceGroupName</span></span>
<span data-ttu-id="9dba5-119">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="9dba5-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="9dba5-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="9dba5-120">-Location</span></span>
<span data-ttu-id="9dba5-121">Helyre</span><span class="sxs-lookup"><span data-stu-id="9dba5-121">Location</span></span> 

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

### <span data-ttu-id="9dba5-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9dba5-122">-Name</span></span>
<span data-ttu-id="9dba5-123">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="9dba5-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="9dba5-124">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="9dba5-124">-NumberofWorkers</span></span>
<span data-ttu-id="9dba5-125">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="9dba5-125">Number Of Workers</span></span>

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

### <span data-ttu-id="9dba5-126">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="9dba5-126">-PerSiteScaling</span></span>
<span data-ttu-id="9dba5-127">A webhelyek méretezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="9dba5-127">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="9dba5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dba5-128">-ResourceGroupName</span></span>
<span data-ttu-id="9dba5-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="9dba5-129">Resource Group Name</span></span>

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

### <span data-ttu-id="9dba5-130">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="9dba5-130">-Tier</span></span>
<span data-ttu-id="9dba5-131">Tier</span><span class="sxs-lookup"><span data-stu-id="9dba5-131">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dba5-132">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="9dba5-132">-WorkerSize</span></span>
<span data-ttu-id="9dba5-133">Webes munkatárs mérete</span><span class="sxs-lookup"><span data-stu-id="9dba5-133">Size of web worker</span></span>

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

### <span data-ttu-id="9dba5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dba5-134">-DefaultProfile</span></span>
<span data-ttu-id="9dba5-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dba5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dba5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dba5-136">CommonParameters</span></span>
<span data-ttu-id="9dba5-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dba5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dba5-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dba5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dba5-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dba5-139">INPUTS</span></span>

### <span data-ttu-id="9dba5-140">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="9dba5-140">ServerFarmWithRichSku</span></span>
<span data-ttu-id="9dba5-141">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="9dba5-141">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="9dba5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dba5-142">OUTPUTS</span></span>

### <span data-ttu-id="9dba5-143">Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="9dba5-143">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="9dba5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dba5-144">NOTES</span></span>

## <span data-ttu-id="9dba5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dba5-145">RELATED LINKS</span></span>

[<span data-ttu-id="9dba5-146">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9dba5-146">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="9dba5-147">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9dba5-147">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="9dba5-148">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9dba5-148">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


