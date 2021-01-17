---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: a81bb1515e25f9000438fbd463117e4fd69b9690
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466097"
---
# <span data-ttu-id="1051e-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="1051e-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="1051e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1051e-102">SYNOPSIS</span></span>
<span data-ttu-id="1051e-103">Funkcióalkalmazásokat kap egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1051e-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="1051e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1051e-104">SYNTAX</span></span>

### <span data-ttu-id="1051e-105">GetAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1051e-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1051e-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="1051e-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1051e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="1051e-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1051e-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1051e-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1051e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1051e-109">DESCRIPTION</span></span>
<span data-ttu-id="1051e-110">Funkcióalkalmazásokat kap egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1051e-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="1051e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1051e-111">EXAMPLES</span></span>

### <span data-ttu-id="1051e-112">1. példa: Az összes függvényalkalmazás letöltése.</span><span class="sxs-lookup"><span data-stu-id="1051e-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="1051e-113">2. példa: Függvényalkalmazások letöltése név szerint.</span><span class="sxs-lookup"><span data-stu-id="1051e-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="1051e-114">3. példa: Függvényalkalmazások lekérte az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="1051e-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="1051e-115">4. példa: Függvényalkalmazások letöltése az adott előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="1051e-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="1051e-116">5. példa: Függvényalkalmazások lekérte hely szerint.</span><span class="sxs-lookup"><span data-stu-id="1051e-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="1051e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1051e-117">PARAMETERS</span></span>

### <span data-ttu-id="1051e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1051e-118">-DefaultProfile</span></span>
<span data-ttu-id="1051e-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1051e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1051e-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="1051e-120">-IncludeSlot</span></span>
<span data-ttu-id="1051e-121">Itt adhatja meg, hogy szerepeljenek-e az üzembe helyezési rések a találatok között.</span><span class="sxs-lookup"><span data-stu-id="1051e-121">Use to specify whether to include deployment slots in results.</span></span>

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

### <span data-ttu-id="1051e-122">-Location</span><span class="sxs-lookup"><span data-stu-id="1051e-122">-Location</span></span>
<span data-ttu-id="1051e-123">A függvényalkalmazás helye.</span><span class="sxs-lookup"><span data-stu-id="1051e-123">The location of the function app.</span></span>

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

### <span data-ttu-id="1051e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1051e-124">-Name</span></span>
<span data-ttu-id="1051e-125">A függvényalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="1051e-125">The name of the function app.</span></span>

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

### <span data-ttu-id="1051e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1051e-126">-ResourceGroupName</span></span>
<span data-ttu-id="1051e-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1051e-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="1051e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1051e-128">-SubscriptionId</span></span>
<span data-ttu-id="1051e-129">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1051e-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="1051e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1051e-130">CommonParameters</span></span>
<span data-ttu-id="1051e-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1051e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1051e-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1051e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1051e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1051e-133">INPUTS</span></span>

## <span data-ttu-id="1051e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1051e-134">OUTPUTS</span></span>

### <span data-ttu-id="1051e-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="1051e-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="1051e-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1051e-136">NOTES</span></span>

<span data-ttu-id="1051e-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1051e-137">ALIASES</span></span>

## <span data-ttu-id="1051e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1051e-138">RELATED LINKS</span></span>

