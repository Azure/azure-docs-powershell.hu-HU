---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159714"
---
# <span data-ttu-id="51583-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="51583-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="51583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51583-102">SYNOPSIS</span></span>
<span data-ttu-id="51583-103">Függvényalkalmazás-csomagokat is lekért egy előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="51583-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="51583-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="51583-104">SYNTAX</span></span>

### <span data-ttu-id="51583-105">GetAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="51583-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51583-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="51583-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="51583-107">ByName</span><span class="sxs-lookup"><span data-stu-id="51583-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="51583-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51583-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="51583-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="51583-109">DESCRIPTION</span></span>
<span data-ttu-id="51583-110">Függvényalkalmazás-csomagokat is lekért egy előfizetésbe.</span><span class="sxs-lookup"><span data-stu-id="51583-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="51583-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="51583-111">EXAMPLES</span></span>

### <span data-ttu-id="51583-112">1. példa: Az összes függvényalkalmazás-csomag letöltése.</span><span class="sxs-lookup"><span data-stu-id="51583-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="51583-113">Ez a parancs az összes funkcióalkalmazás-tervet beveszi.</span><span class="sxs-lookup"><span data-stu-id="51583-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="51583-114">2. példa: Függvényalkalmazástervek lekérte erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="51583-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="51583-115">Ez a parancs a függvényalkalmazásterveket erőforráscsoport neve alapján kapja meg.</span><span class="sxs-lookup"><span data-stu-id="51583-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="51583-116">3. példa: Függvényalkalmazás-csomagok letöltése az adott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="51583-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="51583-117">Ez a parancs függvényalkalmazás-csomagokat kap az adott előfizetések esetén.</span><span class="sxs-lookup"><span data-stu-id="51583-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="51583-118">4. példa: Függvényalkalmazástervek lekérte hely szerint.</span><span class="sxs-lookup"><span data-stu-id="51583-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="51583-119">Ez a parancs funkcióalkalmazásterveket kap hely szerint.</span><span class="sxs-lookup"><span data-stu-id="51583-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="51583-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51583-120">PARAMETERS</span></span>

### <span data-ttu-id="51583-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51583-121">-DefaultProfile</span></span>
<span data-ttu-id="51583-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51583-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51583-123">-Location</span><span class="sxs-lookup"><span data-stu-id="51583-123">-Location</span></span>
<span data-ttu-id="51583-124">A függvényalkalmazás-terv helye.</span><span class="sxs-lookup"><span data-stu-id="51583-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51583-125">-Name</span><span class="sxs-lookup"><span data-stu-id="51583-125">-Name</span></span>
<span data-ttu-id="51583-126">A szolgáltatásterv neve.</span><span class="sxs-lookup"><span data-stu-id="51583-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51583-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51583-127">-ResourceGroupName</span></span>
<span data-ttu-id="51583-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="51583-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51583-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51583-129">-SubscriptionId</span></span>
<span data-ttu-id="51583-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="51583-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51583-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51583-131">CommonParameters</span></span>
<span data-ttu-id="51583-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51583-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51583-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51583-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51583-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51583-134">INPUTS</span></span>

## <span data-ttu-id="51583-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51583-135">OUTPUTS</span></span>

### <span data-ttu-id="51583-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="51583-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="51583-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="51583-137">NOTES</span></span>

<span data-ttu-id="51583-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="51583-138">ALIASES</span></span>

## <span data-ttu-id="51583-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51583-139">RELATED LINKS</span></span>

