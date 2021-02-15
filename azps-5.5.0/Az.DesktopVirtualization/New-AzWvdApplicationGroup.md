---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: bbbdd1a3cd324a57d4889e3afe01f387bc5b478e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209743"
---
# <span data-ttu-id="298b2-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="298b2-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="298b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="298b2-102">SYNOPSIS</span></span>
<span data-ttu-id="298b2-103">Hozzon létre vagy frissítsen egy applicationGroup csoportot.</span><span class="sxs-lookup"><span data-stu-id="298b2-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="298b2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="298b2-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="298b2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="298b2-105">DESCRIPTION</span></span>
<span data-ttu-id="298b2-106">Hozzon létre vagy frissítsen egy applicationGroup csoportot.</span><span class="sxs-lookup"><span data-stu-id="298b2-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="298b2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="298b2-107">EXAMPLES</span></span>

### <span data-ttu-id="298b2-108">1. példa: Windows Virtuális asztali alkalmazáscsoport létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="298b2-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="298b2-109">Ez a parancs létrehoz egy Windows virtuális asztali alkalmazáscsoportot egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="298b2-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="298b2-110">2. példa: Windows Virtuális asztali alkalmazáscsoport létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="298b2-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="298b2-111">Ez a parancs létrehoz egy Windows virtuális asztali alkalmazáscsoportot egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="298b2-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="298b2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="298b2-112">PARAMETERS</span></span>

### <span data-ttu-id="298b2-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="298b2-113">-ApplicationGroupType</span></span>
<span data-ttu-id="298b2-114">Az ApplicationGroup erőforrástípusa.</span><span class="sxs-lookup"><span data-stu-id="298b2-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="298b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298b2-115">-DefaultProfile</span></span>
<span data-ttu-id="298b2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="298b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="298b2-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="298b2-117">-Description</span></span>
<span data-ttu-id="298b2-118">Az ApplicationGroup leírása.</span><span class="sxs-lookup"><span data-stu-id="298b2-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="298b2-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="298b2-119">-FriendlyName</span></span>
<span data-ttu-id="298b2-120">Az ApplicationGroup rövid neve.</span><span class="sxs-lookup"><span data-stu-id="298b2-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="298b2-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="298b2-121">-HostPoolArmPath</span></span>
<span data-ttu-id="298b2-122">Az ApplicationGroup HostPool-kar útvonala.</span><span class="sxs-lookup"><span data-stu-id="298b2-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="298b2-123">-Location</span><span class="sxs-lookup"><span data-stu-id="298b2-123">-Location</span></span>
<span data-ttu-id="298b2-124">Az a földrajzi hely, ahol az erőforrás található</span><span class="sxs-lookup"><span data-stu-id="298b2-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="298b2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="298b2-125">-Name</span></span>
<span data-ttu-id="298b2-126">Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="298b2-126">The name of the application group</span></span>

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

### <span data-ttu-id="298b2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="298b2-127">-ResourceGroupName</span></span>
<span data-ttu-id="298b2-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="298b2-128">The name of the resource group.</span></span>
<span data-ttu-id="298b2-129">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="298b2-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="298b2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="298b2-130">-SubscriptionId</span></span>
<span data-ttu-id="298b2-131">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="298b2-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="298b2-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="298b2-132">-Tag</span></span>
<span data-ttu-id="298b2-133">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="298b2-133">Resource tags.</span></span>

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

### <span data-ttu-id="298b2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="298b2-134">-Confirm</span></span>
<span data-ttu-id="298b2-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="298b2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="298b2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="298b2-136">-WhatIf</span></span>
<span data-ttu-id="298b2-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="298b2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="298b2-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="298b2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="298b2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298b2-139">CommonParameters</span></span>
<span data-ttu-id="298b2-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="298b2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298b2-141">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="298b2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298b2-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="298b2-142">INPUTS</span></span>

## <span data-ttu-id="298b2-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="298b2-143">OUTPUTS</span></span>

### <span data-ttu-id="298b2-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="298b2-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup</span></span>

## <span data-ttu-id="298b2-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="298b2-145">NOTES</span></span>

<span data-ttu-id="298b2-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="298b2-146">ALIASES</span></span>

## <span data-ttu-id="298b2-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="298b2-147">RELATED LINKS</span></span>

