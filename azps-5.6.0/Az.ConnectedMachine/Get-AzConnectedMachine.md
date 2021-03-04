---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachine.md
ms.openlocfilehash: c97567c2832d82ec739b62bfe8bb6c08e173f9e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012406"
---
# <span data-ttu-id="ecc1d-101">Get-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="ecc1d-101">Get-AzConnectedMachine</span></span>

## <span data-ttu-id="ecc1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecc1d-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc1d-103">Beolvassa a hibrid számítógép modellnézetével vagy példánynézetével kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-103">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="ecc1d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ecc1d-104">SYNTAX</span></span>

### <span data-ttu-id="ecc1d-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ecc1d-105">List1 (Default)</span></span>
```
Get-AzConnectedMachine [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ecc1d-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="ecc1d-106">Get</span></span>
```
Get-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ecc1d-107">Lista</span><span class="sxs-lookup"><span data-stu-id="ecc1d-107">List</span></span>
```
Get-AzConnectedMachine -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ecc1d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ecc1d-108">DESCRIPTION</span></span>
<span data-ttu-id="ecc1d-109">Beolvassa a hibrid számítógép modellnézetével vagy példánynézetével kapcsolatos információkat.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-109">Retrieves information about the model view or the instance view of a hybrid machine.</span></span>

## <span data-ttu-id="ecc1d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ecc1d-110">EXAMPLES</span></span>

### <span data-ttu-id="ecc1d-111">1. példa: Az előfizetés összes csatlakoztatott számítógépének felsorolása</span><span class="sxs-lookup"><span data-stu-id="ecc1d-111">Example 1: List all connected machines in a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -SubscriptionId 67379433-5e19-4702-b39a-c0a03ca8d20c

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
linwestus2_1   westus2  linux    Connected  Succeeded
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded

```

<span data-ttu-id="ecc1d-112">Az előfizetésben található összes csatlakoztatott gép listája.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-112">Lists all connected machines in a subscription.</span></span>
<span data-ttu-id="ecc1d-113">Ha nincs megadva előfizetés, az aktuális Azure PowerShell-környezetből fogja használni az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-113">If subscription isn't specified, it will use the subscription from your current Azure PowerShell context.</span></span>

### <span data-ttu-id="ecc1d-114">2. példa: Egy erőforráscsoport összes csatlakoztatott gépének felsorolása</span><span class="sxs-lookup"><span data-stu-id="ecc1d-114">Example 2: List all connected machines in a resource group</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_2   westus2  windows  Connected  Succeeded
winwestus2_3   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="ecc1d-115">List all connected machines in a resource group.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-115">List all connected machines in a resource group.</span></span>

### <span data-ttu-id="ecc1d-116">3. példa: Csatlakoztatott számítógép lekérte egy erőforráscsoportba név szerint</span><span class="sxs-lookup"><span data-stu-id="ecc1d-116">Example 3: Get a connected machine in a resource group by name</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines -Name winwestus2_1

Name           Location OSName   Status     ProvisioningState
----           -------- ------   ------     -----------------
winwestus2_1   westus2  windows  Connected  Succeeded
```

<span data-ttu-id="ecc1d-117">Csatlakoztatott gép lekérte egy erőforráscsoporthoz név szerint.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-117">Get a connected machine in a resource group by name.</span></span>

## <span data-ttu-id="ecc1d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecc1d-118">PARAMETERS</span></span>

### <span data-ttu-id="ecc1d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc1d-119">-DefaultProfile</span></span>
<span data-ttu-id="ecc1d-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc1d-121">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="ecc1d-121">-Expand</span></span>
<span data-ttu-id="ecc1d-122">A műveletre alkalmazandó kibontó kifejezés.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-122">The expand expression to apply on the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Support.InstanceViewTypes
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc1d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ecc1d-123">-Name</span></span>
<span data-ttu-id="ecc1d-124">A hibrid gép neve.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-124">The name of the hybrid machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="ecc1d-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc1d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ecc1d-127">-SubscriptionId</span></span>
<span data-ttu-id="ecc1d-128">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ecc1d-129">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ecc1d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc1d-130">CommonParameters</span></span>
<span data-ttu-id="ecc1d-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc1d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc1d-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecc1d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc1d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ecc1d-133">INPUTS</span></span>

## <span data-ttu-id="ecc1d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ecc1d-134">OUTPUTS</span></span>

### <span data-ttu-id="ecc1d-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span><span class="sxs-lookup"><span data-stu-id="ecc1d-135">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachine</span></span>

## <span data-ttu-id="ecc1d-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ecc1d-136">NOTES</span></span>

<span data-ttu-id="ecc1d-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="ecc1d-137">ALIASES</span></span>

## <span data-ttu-id="ecc1d-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ecc1d-138">RELATED LINKS</span></span>

