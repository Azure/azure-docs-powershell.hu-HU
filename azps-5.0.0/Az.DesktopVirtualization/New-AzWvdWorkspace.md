---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: fbd71d03c6f82bcb785105d9d75e155e9f7ef498
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297023"
---
# <span data-ttu-id="90dd2-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="90dd2-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="90dd2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="90dd2-103">Munkaterület létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="90dd2-103">Create or update a workspace.</span></span>

## <span data-ttu-id="90dd2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90dd2-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90dd2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90dd2-105">DESCRIPTION</span></span>
<span data-ttu-id="90dd2-106">Munkaterület létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="90dd2-106">Create or update a workspace.</span></span>

## <span data-ttu-id="90dd2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90dd2-107">EXAMPLES</span></span>

### <span data-ttu-id="90dd2-108">Példa 1: a Windows virtuális asztali Worksapce létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="90dd2-108">Example 1: Create a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference $null `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="90dd2-109">Ez a parancs egy Windows virtuális asztali munkaterületet hoz létre egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="90dd2-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="90dd2-110">2. példa: a Windows virtuális asztali Worksapce létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="90dd2-110">Example 2: Create a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> New-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -Location 'eastus' `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="90dd2-111">Ez a parancs egy Windows virtuális asztali munkaterületet hoz létre egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="90dd2-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="90dd2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90dd2-112">PARAMETERS</span></span>

### <span data-ttu-id="90dd2-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="90dd2-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="90dd2-114">ApplicationGroup-erőforrás-azonosítók listája</span><span class="sxs-lookup"><span data-stu-id="90dd2-114">List of applicationGroup resource Ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90dd2-115">-DefaultProfile</span></span>
<span data-ttu-id="90dd2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90dd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90dd2-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="90dd2-117">-Description</span></span>
<span data-ttu-id="90dd2-118">A munkaterület leírása.</span><span class="sxs-lookup"><span data-stu-id="90dd2-118">Description of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dd2-119">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="90dd2-119">-FriendlyName</span></span>
<span data-ttu-id="90dd2-120">A munkaterület rövid neve.</span><span class="sxs-lookup"><span data-stu-id="90dd2-120">Friendly name of Workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dd2-121">-Hely</span><span class="sxs-lookup"><span data-stu-id="90dd2-121">-Location</span></span>
<span data-ttu-id="90dd2-122">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="90dd2-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="90dd2-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90dd2-123">-Name</span></span>
<span data-ttu-id="90dd2-124">A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="90dd2-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dd2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90dd2-125">-ResourceGroupName</span></span>
<span data-ttu-id="90dd2-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="90dd2-126">The name of the resource group.</span></span>
<span data-ttu-id="90dd2-127">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="90dd2-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="90dd2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90dd2-128">-SubscriptionId</span></span>
<span data-ttu-id="90dd2-129">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="90dd2-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dd2-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="90dd2-130">-Tag</span></span>
<span data-ttu-id="90dd2-131">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="90dd2-131">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dd2-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="90dd2-132">-Confirm</span></span>
<span data-ttu-id="90dd2-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="90dd2-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dd2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90dd2-134">-WhatIf</span></span>
<span data-ttu-id="90dd2-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="90dd2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90dd2-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="90dd2-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dd2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90dd2-137">CommonParameters</span></span>
<span data-ttu-id="90dd2-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90dd2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90dd2-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="90dd2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90dd2-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90dd2-140">INPUTS</span></span>

## <span data-ttu-id="90dd2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90dd2-141">OUTPUTS</span></span>

### <span data-ttu-id="90dd2-142">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="90dd2-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IWorkspace</span></span>

## <span data-ttu-id="90dd2-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90dd2-143">NOTES</span></span>

<span data-ttu-id="90dd2-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="90dd2-144">ALIASES</span></span>

## <span data-ttu-id="90dd2-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90dd2-145">RELATED LINKS</span></span>

