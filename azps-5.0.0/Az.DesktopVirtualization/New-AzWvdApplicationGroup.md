---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297044"
---
# <span data-ttu-id="e0fc3-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="e0fc3-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="e0fc3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="e0fc3-103">ApplicationGroup létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="e0fc3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0fc3-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e0fc3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="e0fc3-106">ApplicationGroup létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="e0fc3-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="e0fc3-108">Példa 1: a Windows virtuális asztali ApplicationGroup létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="e0fc3-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="e0fc3-109">Ez a parancs létrehoz egy Windows virtuális asztali ApplicationGroup egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="e0fc3-110">2. példa: a Windows virtuális asztali ApplicationGroup létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="e0fc3-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
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

<span data-ttu-id="e0fc3-111">Ez a parancs létrehoz egy Windows virtuális asztali ApplicationGroup egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="e0fc3-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0fc3-112">PARAMETERS</span></span>

### <span data-ttu-id="e0fc3-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="e0fc3-113">-ApplicationGroupType</span></span>
<span data-ttu-id="e0fc3-114">Az ApplicationGroup erőforrás típusa.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-114">Resource Type of ApplicationGroup.</span></span>

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

### <span data-ttu-id="e0fc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0fc3-115">-DefaultProfile</span></span>
<span data-ttu-id="e0fc3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0fc3-117">-Leírás</span><span class="sxs-lookup"><span data-stu-id="e0fc3-117">-Description</span></span>
<span data-ttu-id="e0fc3-118">A ApplicationGroup leírása.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-118">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="e0fc3-119">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="e0fc3-119">-FriendlyName</span></span>
<span data-ttu-id="e0fc3-120">A ApplicationGroup rövid neve.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-120">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="e0fc3-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="e0fc3-121">-HostPoolArmPath</span></span>
<span data-ttu-id="e0fc3-122">A ApplicationGroup HostPool kar elérési útja.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="e0fc3-123">-Hely</span><span class="sxs-lookup"><span data-stu-id="e0fc3-123">-Location</span></span>
<span data-ttu-id="e0fc3-124">Az a földrajzi hely, ahol az erőforrás él</span><span class="sxs-lookup"><span data-stu-id="e0fc3-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="e0fc3-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e0fc3-125">-Name</span></span>
<span data-ttu-id="e0fc3-126">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="e0fc3-126">The name of the application group</span></span>

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

### <span data-ttu-id="e0fc3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0fc3-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0fc3-128">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-128">The name of the resource group.</span></span>
<span data-ttu-id="e0fc3-129">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e0fc3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0fc3-130">-SubscriptionId</span></span>
<span data-ttu-id="e0fc3-131">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e0fc3-132">-Címke</span><span class="sxs-lookup"><span data-stu-id="e0fc3-132">-Tag</span></span>
<span data-ttu-id="e0fc3-133">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-133">Resource tags.</span></span>

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

### <span data-ttu-id="e0fc3-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0fc3-134">-Confirm</span></span>
<span data-ttu-id="e0fc3-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0fc3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0fc3-136">-WhatIf</span></span>
<span data-ttu-id="e0fc3-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0fc3-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0fc3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0fc3-139">CommonParameters</span></span>
<span data-ttu-id="e0fc3-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0fc3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0fc3-141">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e0fc3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0fc3-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0fc3-142">INPUTS</span></span>

## <span data-ttu-id="e0fc3-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0fc3-143">OUTPUTS</span></span>

### <span data-ttu-id="e0fc3-144">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="e0fc3-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="e0fc3-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0fc3-145">NOTES</span></span>

<span data-ttu-id="e0fc3-146">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e0fc3-146">ALIASES</span></span>

## <span data-ttu-id="e0fc3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0fc3-147">RELATED LINKS</span></span>

