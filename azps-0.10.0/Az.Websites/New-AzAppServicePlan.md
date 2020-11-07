---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 040efd4e483825db637345fbd8bcb54a27e8675b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842753"
---
# <span data-ttu-id="05e8a-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05e8a-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="05e8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="05e8a-103">Azure app-szolgáltatási csomagot hoz létre egy adott földrajzi helyen.</span><span class="sxs-lookup"><span data-stu-id="05e8a-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="05e8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05e8a-104">SYNTAX</span></span>

### <span data-ttu-id="05e8a-105">S1</span><span class="sxs-lookup"><span data-stu-id="05e8a-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05e8a-106">S2</span><span class="sxs-lookup"><span data-stu-id="05e8a-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05e8a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="05e8a-107">DESCRIPTION</span></span>
<span data-ttu-id="05e8a-108">A **New-AzAppServicePlan** parancsmag létrehoz egy Azure app-szolgáltatási csomagot egy adott földrajzi helyen, a megadott szinttel, a munkás méretével és a munkavállalók számával.</span><span class="sxs-lookup"><span data-stu-id="05e8a-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="05e8a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="05e8a-109">EXAMPLES</span></span>

### <span data-ttu-id="05e8a-110">1. példa: alkalmazás-szolgáltatási csomag létrehozása</span><span class="sxs-lookup"><span data-stu-id="05e8a-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="05e8a-111">Ez a parancs létrehoz egy ContosoASP nevű app-szolgáltatási csomagot a Default-Web-WestUS földrajzi helyének West US nevű erőforráscsoport nevű erőforráscsoport nevű csoportjában.</span><span class="sxs-lookup"><span data-stu-id="05e8a-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="05e8a-112">A parancs egy alapszintet határoz meg, és két kisméretű dolgozót oszt szét.</span><span class="sxs-lookup"><span data-stu-id="05e8a-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="05e8a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05e8a-113">PARAMETERS</span></span>

### <span data-ttu-id="05e8a-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05e8a-114">-AppServicePlan</span></span>
<span data-ttu-id="05e8a-115">Alkalmazás-szolgáltatási terv objektum</span><span class="sxs-lookup"><span data-stu-id="05e8a-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="05e8a-116">-AseName</span></span>
<span data-ttu-id="05e8a-117">Alkalmazás-szolgáltatási környezet neve</span><span class="sxs-lookup"><span data-stu-id="05e8a-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e8a-118">-AseResourceGroupName</span></span>
<span data-ttu-id="05e8a-119">Az App szolgáltatás környezeti erőforrás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="05e8a-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e8a-120">-DefaultProfile</span></span>
<span data-ttu-id="05e8a-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05e8a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="05e8a-122">-Location</span></span>
<span data-ttu-id="05e8a-123">Helyre</span><span class="sxs-lookup"><span data-stu-id="05e8a-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05e8a-124">-Name</span></span>
<span data-ttu-id="05e8a-125">Alkalmazás-szolgáltatási terv neve</span><span class="sxs-lookup"><span data-stu-id="05e8a-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="05e8a-126">-NumberofWorkers</span></span>
<span data-ttu-id="05e8a-127">Munkavállalók száma</span><span class="sxs-lookup"><span data-stu-id="05e8a-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="05e8a-128">-PerSiteScaling</span></span>
<span data-ttu-id="05e8a-129">A webhelyek méretezésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="05e8a-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e8a-130">-ResourceGroupName</span></span>
<span data-ttu-id="05e8a-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="05e8a-131">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-132">-Tier (Tier)</span><span class="sxs-lookup"><span data-stu-id="05e8a-132">-Tier</span></span>
<span data-ttu-id="05e8a-133">Tier</span><span class="sxs-lookup"><span data-stu-id="05e8a-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="05e8a-134">-WorkerSize</span></span>
<span data-ttu-id="05e8a-135">Webes munkatárs mérete</span><span class="sxs-lookup"><span data-stu-id="05e8a-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="05e8a-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05e8a-136">-AsJob</span></span>
<span data-ttu-id="05e8a-137">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="05e8a-137">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e8a-138">CommonParameters</span></span>
<span data-ttu-id="05e8a-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05e8a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e8a-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e8a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e8a-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05e8a-141">INPUTS</span></span>

### <span data-ttu-id="05e8a-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="05e8a-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="05e8a-143">A ' AppServicePlan ' paraméter az "ServerFarmWithRichSku" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="05e8a-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="05e8a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05e8a-144">OUTPUTS</span></span>

### <span data-ttu-id="05e8a-145">Microsoft. Azure. Management. WebSites. models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="05e8a-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="05e8a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05e8a-146">NOTES</span></span>

## <span data-ttu-id="05e8a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05e8a-147">RELATED LINKS</span></span>

[<span data-ttu-id="05e8a-148">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05e8a-148">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="05e8a-149">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05e8a-149">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="05e8a-150">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="05e8a-150">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


