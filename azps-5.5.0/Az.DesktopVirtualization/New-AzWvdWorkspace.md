---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdWorkspace.md
ms.openlocfilehash: b97db1a21afab939e94b776b3da8d43f3d1468b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204255"
---
# <span data-ttu-id="8fd58-101">New-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="8fd58-101">New-AzWvdWorkspace</span></span>

## <span data-ttu-id="8fd58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fd58-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd58-103">Munkaterület létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="8fd58-103">Create or update a workspace.</span></span>

## <span data-ttu-id="8fd58-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8fd58-104">SYNTAX</span></span>

```
New-AzWvdWorkspace -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8fd58-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8fd58-105">DESCRIPTION</span></span>
<span data-ttu-id="8fd58-106">Munkaterület létrehozása vagy frissítése.</span><span class="sxs-lookup"><span data-stu-id="8fd58-106">Create or update a workspace.</span></span>

## <span data-ttu-id="8fd58-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8fd58-107">EXAMPLES</span></span>

### <span data-ttu-id="8fd58-108">1. példa: Virtuális asztali Windows-munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="8fd58-108">Example 1: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="8fd58-109">Ez a parancs létrehoz egy Windows virtuális asztal-munkaterületet egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="8fd58-109">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

### <span data-ttu-id="8fd58-110">2. példa: Virtuális asztali Windows-munkaterület létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="8fd58-110">Example 2: Create a Windows Virtual Desktop Workspace by name</span></span>
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

<span data-ttu-id="8fd58-111">Ez a parancs létrehoz egy Windows virtuális asztal-munkaterületet egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="8fd58-111">This command creates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="8fd58-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fd58-112">PARAMETERS</span></span>

### <span data-ttu-id="8fd58-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="8fd58-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="8fd58-114">Az applicationGroup-erőforrásazonosítók listája.</span><span class="sxs-lookup"><span data-stu-id="8fd58-114">List of applicationGroup resource Ids.</span></span>

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

### <span data-ttu-id="8fd58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd58-115">-DefaultProfile</span></span>
<span data-ttu-id="8fd58-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fd58-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fd58-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8fd58-117">-Description</span></span>
<span data-ttu-id="8fd58-118">A Munkaterület leírása.</span><span class="sxs-lookup"><span data-stu-id="8fd58-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="8fd58-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="8fd58-119">-FriendlyName</span></span>
<span data-ttu-id="8fd58-120">A Munkaterület felhasználóbarát neve.</span><span class="sxs-lookup"><span data-stu-id="8fd58-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="8fd58-121">-Location</span><span class="sxs-lookup"><span data-stu-id="8fd58-121">-Location</span></span>
<span data-ttu-id="8fd58-122">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="8fd58-122">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="8fd58-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8fd58-123">-Name</span></span>
<span data-ttu-id="8fd58-124">A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="8fd58-124">The name of the workspace</span></span>

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

### <span data-ttu-id="8fd58-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd58-125">-ResourceGroupName</span></span>
<span data-ttu-id="8fd58-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fd58-126">The name of the resource group.</span></span>
<span data-ttu-id="8fd58-127">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="8fd58-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8fd58-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fd58-128">-SubscriptionId</span></span>
<span data-ttu-id="8fd58-129">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8fd58-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8fd58-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="8fd58-130">-Tag</span></span>
<span data-ttu-id="8fd58-131">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="8fd58-131">Resource tags.</span></span>

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

### <span data-ttu-id="8fd58-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fd58-132">-Confirm</span></span>
<span data-ttu-id="8fd58-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8fd58-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd58-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd58-134">-WhatIf</span></span>
<span data-ttu-id="8fd58-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8fd58-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd58-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8fd58-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd58-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd58-137">CommonParameters</span></span>
<span data-ttu-id="8fd58-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd58-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd58-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fd58-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd58-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8fd58-140">INPUTS</span></span>

## <span data-ttu-id="8fd58-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fd58-141">OUTPUTS</span></span>

### <span data-ttu-id="8fd58-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="8fd58-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IWorkspace</span></span>

## <span data-ttu-id="8fd58-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8fd58-143">NOTES</span></span>

<span data-ttu-id="8fd58-144">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8fd58-144">ALIASES</span></span>

## <span data-ttu-id="8fd58-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fd58-145">RELATED LINKS</span></span>

