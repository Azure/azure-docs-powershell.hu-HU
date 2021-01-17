---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: bbbdd1a3cd324a57d4889e3afe01f387bc5b478e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469930"
---
# <span data-ttu-id="4b265-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4b265-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="4b265-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b265-102">SYNOPSIS</span></span>
<span data-ttu-id="4b265-103">Hozzon létre vagy frissítsen egy applicationGroup csoportot.</span><span class="sxs-lookup"><span data-stu-id="4b265-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="4b265-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b265-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b265-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b265-105">DESCRIPTION</span></span>
<span data-ttu-id="4b265-106">Hozzon létre vagy frissítsen egy applicationGroup csoportot.</span><span class="sxs-lookup"><span data-stu-id="4b265-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="4b265-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b265-107">EXAMPLES</span></span>

### <span data-ttu-id="4b265-108">1. példa: Windows Virtuális asztali alkalmazáscsoport létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="4b265-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="4b265-109">Ez a parancs létrehoz egy Windows virtuális asztali alkalmazáscsoportot egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="4b265-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="4b265-110">2. példa: Windows Virtuális asztali alkalmazáscsoport létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="4b265-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="4b265-111">Ez a parancs létrehoz egy Windows virtuális asztali alkalmazáscsoportot egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="4b265-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="4b265-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b265-112">PARAMETERS</span></span>

### <span data-ttu-id="4b265-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="4b265-113">-ApplicationGroupType</span></span>
<span data-ttu-id="4b265-114">Az ApplicationGroup erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="4b265-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b265-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b265-115">-DefaultProfile</span></span>
<span data-ttu-id="4b265-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b265-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b265-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="4b265-117">-Description</span></span>
<span data-ttu-id="4b265-118">Az ApplicationGroup leírása.</span><span class="sxs-lookup"><span data-stu-id="4b265-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4b265-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4b265-119">-FriendlyName</span></span>
<span data-ttu-id="4b265-120">Az ApplicationGroup rövid neve.</span><span class="sxs-lookup"><span data-stu-id="4b265-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4b265-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="4b265-121">-HostPoolArmPath</span></span>
<span data-ttu-id="4b265-122">Az ApplicationGroup HostPool-kar útvonala.</span><span class="sxs-lookup"><span data-stu-id="4b265-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="4b265-123">-Location</span><span class="sxs-lookup"><span data-stu-id="4b265-123">-Location</span></span>
<span data-ttu-id="4b265-124">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="4b265-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="4b265-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4b265-125">-Name</span></span>
<span data-ttu-id="4b265-126">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="4b265-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b265-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b265-127">-ResourceGroupName</span></span>
<span data-ttu-id="4b265-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4b265-128">The name of the resource group.</span></span>
<span data-ttu-id="4b265-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="4b265-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4b265-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b265-130">-SubscriptionId</span></span>
<span data-ttu-id="4b265-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="4b265-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4b265-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b265-132">-Tag</span></span>
<span data-ttu-id="4b265-133">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="4b265-133">Resource tags.</span></span>

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

### <span data-ttu-id="4b265-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b265-134">-Confirm</span></span>
<span data-ttu-id="4b265-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4b265-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b265-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b265-136">-WhatIf</span></span>
<span data-ttu-id="4b265-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4b265-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b265-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4b265-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b265-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b265-139">CommonParameters</span></span>
<span data-ttu-id="4b265-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b265-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b265-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b265-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b265-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b265-142">INPUTS</span></span>

## <span data-ttu-id="4b265-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b265-143">OUTPUTS</span></span>

### <span data-ttu-id="4b265-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="4b265-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="4b265-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b265-145">NOTES</span></span>

<span data-ttu-id="4b265-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="4b265-146">ALIASES</span></span>

## <span data-ttu-id="4b265-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b265-147">RELATED LINKS</span></span>

