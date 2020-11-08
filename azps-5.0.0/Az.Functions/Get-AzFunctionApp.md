---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185432"
---
# <span data-ttu-id="dc883-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="dc883-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="dc883-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dc883-102">SYNOPSIS</span></span>
<span data-ttu-id="dc883-103">Beolvassa az előfizetésben az alkalmazások függvényt.</span><span class="sxs-lookup"><span data-stu-id="dc883-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="dc883-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dc883-104">SYNTAX</span></span>

### <span data-ttu-id="dc883-105">GetAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dc883-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc883-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="dc883-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc883-107">ByName</span><span class="sxs-lookup"><span data-stu-id="dc883-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dc883-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc883-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dc883-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="dc883-109">DESCRIPTION</span></span>
<span data-ttu-id="dc883-110">Beolvassa az előfizetésben az alkalmazások függvényt.</span><span class="sxs-lookup"><span data-stu-id="dc883-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="dc883-111">Példák</span><span class="sxs-lookup"><span data-stu-id="dc883-111">EXAMPLES</span></span>

### <span data-ttu-id="dc883-112">1. példa: a minden függvény alkalmazásai beolvasása</span><span class="sxs-lookup"><span data-stu-id="dc883-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="dc883-113">2. példa: a függvények beolvasása név szerint.</span><span class="sxs-lookup"><span data-stu-id="dc883-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="dc883-114">3. példa: a függvények beszerzése az erőforráscsoport nevével</span><span class="sxs-lookup"><span data-stu-id="dc883-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="dc883-115">4. példa: az adott előfizetéshez tartozó alkalmazások beszerzése.</span><span class="sxs-lookup"><span data-stu-id="dc883-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="dc883-116">Példa 5: az alkalmazások beszerzése hely szerint.</span><span class="sxs-lookup"><span data-stu-id="dc883-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="dc883-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dc883-117">PARAMETERS</span></span>

### <span data-ttu-id="dc883-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc883-118">-DefaultProfile</span></span>
<span data-ttu-id="dc883-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dc883-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc883-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="dc883-120">-IncludeSlot</span></span>
<span data-ttu-id="dc883-121">A beállítással megadhatja, hogy megjelenjenek-e a telepítő bővítőhelyek az eredmények között.</span><span class="sxs-lookup"><span data-stu-id="dc883-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc883-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="dc883-122">-Location</span></span>
<span data-ttu-id="dc883-123">A függvény app helye.</span><span class="sxs-lookup"><span data-stu-id="dc883-123">The location of the function app.</span></span>

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

### <span data-ttu-id="dc883-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dc883-124">-Name</span></span>
<span data-ttu-id="dc883-125">A függvény app neve.</span><span class="sxs-lookup"><span data-stu-id="dc883-125">The name of the function app.</span></span>

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

### <span data-ttu-id="dc883-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc883-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc883-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="dc883-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="dc883-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc883-128">-SubscriptionId</span></span>
<span data-ttu-id="dc883-129">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="dc883-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="dc883-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc883-130">CommonParameters</span></span>
<span data-ttu-id="dc883-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dc883-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc883-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dc883-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc883-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc883-133">INPUTS</span></span>

## <span data-ttu-id="dc883-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dc883-134">OUTPUTS</span></span>

### <span data-ttu-id="dc883-135">Microsoft. Azure. PowerShell. parancsmagok. functions. models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="dc883-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="dc883-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dc883-136">NOTES</span></span>

<span data-ttu-id="dc883-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="dc883-137">ALIASES</span></span>

## <span data-ttu-id="dc883-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dc883-138">RELATED LINKS</span></span>

