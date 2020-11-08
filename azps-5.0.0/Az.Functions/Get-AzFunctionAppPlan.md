---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185429"
---
# <span data-ttu-id="77b8d-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="77b8d-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="77b8d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="77b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="77b8d-103">Egy előfizetésben a Function apps csomagok beszerzése</span><span class="sxs-lookup"><span data-stu-id="77b8d-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="77b8d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="77b8d-104">SYNTAX</span></span>

### <span data-ttu-id="77b8d-105">GetAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77b8d-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="77b8d-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="77b8d-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="77b8d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="77b8d-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="77b8d-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b8d-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="77b8d-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="77b8d-109">DESCRIPTION</span></span>
<span data-ttu-id="77b8d-110">Egy előfizetésben a Function apps csomagok beszerzése</span><span class="sxs-lookup"><span data-stu-id="77b8d-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="77b8d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="77b8d-111">EXAMPLES</span></span>

### <span data-ttu-id="77b8d-112">Példa 1: az összes függvény app-csomag beszerzése.</span><span class="sxs-lookup"><span data-stu-id="77b8d-112">Example 1: Get all function app plans.</span></span>
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

<span data-ttu-id="77b8d-113">Ez a parancs az összes függvény app-csomagot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="77b8d-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="77b8d-114">2. példa: a Function app-csomagok beolvasása az erőforráscsoport nevével</span><span class="sxs-lookup"><span data-stu-id="77b8d-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="77b8d-115">Ez a parancs az erőforráscsoport neve alapján válik elérhetővé az alkalmazásban.</span><span class="sxs-lookup"><span data-stu-id="77b8d-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="77b8d-116">3. példa: az adott előfizetéshez tartozó Function app-csomagok beszerzése.</span><span class="sxs-lookup"><span data-stu-id="77b8d-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="77b8d-117">Ez a parancs a megadott előfizetésekhez tartozó alkalmazás-csomagokat kapja.</span><span class="sxs-lookup"><span data-stu-id="77b8d-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="77b8d-118">4. példa: a Function app csomagok beszerzése hely szerint.</span><span class="sxs-lookup"><span data-stu-id="77b8d-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="77b8d-119">Ez a parancs hely szerint kapja meg az App-csomagok működését.</span><span class="sxs-lookup"><span data-stu-id="77b8d-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="77b8d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="77b8d-120">PARAMETERS</span></span>

### <span data-ttu-id="77b8d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b8d-121">-DefaultProfile</span></span>
<span data-ttu-id="77b8d-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77b8d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77b8d-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="77b8d-123">-Location</span></span>
<span data-ttu-id="77b8d-124">A Function app-csomag helye.</span><span class="sxs-lookup"><span data-stu-id="77b8d-124">The location of the function app plan.</span></span>

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

### <span data-ttu-id="77b8d-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="77b8d-125">-Name</span></span>
<span data-ttu-id="77b8d-126">A szolgáltatás tervének neve.</span><span class="sxs-lookup"><span data-stu-id="77b8d-126">The service plan name.</span></span>

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

### <span data-ttu-id="77b8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77b8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="77b8d-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="77b8d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="77b8d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77b8d-129">-SubscriptionId</span></span>
<span data-ttu-id="77b8d-130">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="77b8d-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="77b8d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b8d-131">CommonParameters</span></span>
<span data-ttu-id="77b8d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="77b8d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b8d-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="77b8d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b8d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="77b8d-134">INPUTS</span></span>

## <span data-ttu-id="77b8d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77b8d-135">OUTPUTS</span></span>

### <span data-ttu-id="77b8d-136">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="77b8d-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="77b8d-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="77b8d-137">NOTES</span></span>

<span data-ttu-id="77b8d-138">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="77b8d-138">ALIASES</span></span>

## <span data-ttu-id="77b8d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77b8d-139">RELATED LINKS</span></span>

