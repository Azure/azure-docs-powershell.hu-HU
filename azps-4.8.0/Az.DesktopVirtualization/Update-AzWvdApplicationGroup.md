---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: ab1f338be9d983efceac0045fec96b1a63fb66bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025369"
---
# <span data-ttu-id="6eace-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="6eace-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="6eace-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6eace-102">SYNOPSIS</span></span>
<span data-ttu-id="6eace-103">Frissítsen egy applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="6eace-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="6eace-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6eace-104">SYNTAX</span></span>

### <span data-ttu-id="6eace-105">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6eace-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6eace-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6eace-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="6eace-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6eace-107">DESCRIPTION</span></span>
<span data-ttu-id="6eace-108">Frissítsen egy applicationGroup.</span><span class="sxs-lookup"><span data-stu-id="6eace-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="6eace-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6eace-109">EXAMPLES</span></span>

### <span data-ttu-id="6eace-110">Példa 1: a Windows virtuális asztali ApplicationGroup létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="6eace-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="6eace-111">Ez a parancs létrehoz egy Windows virtuális asztali ApplicationGroup egy Erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="6eace-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="6eace-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6eace-112">PARAMETERS</span></span>

### <span data-ttu-id="6eace-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eace-113">-DefaultProfile</span></span>
<span data-ttu-id="6eace-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6eace-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eace-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="6eace-115">-Description</span></span>
<span data-ttu-id="6eace-116">A ApplicationGroup leírása.</span><span class="sxs-lookup"><span data-stu-id="6eace-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="6eace-117">-Típusú megjelenített</span><span class="sxs-lookup"><span data-stu-id="6eace-117">-FriendlyName</span></span>
<span data-ttu-id="6eace-118">A ApplicationGroup rövid neve.</span><span class="sxs-lookup"><span data-stu-id="6eace-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="6eace-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eace-119">-InputObject</span></span>
<span data-ttu-id="6eace-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6eace-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6eace-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6eace-121">-Name</span></span>
<span data-ttu-id="6eace-122">Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="6eace-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eace-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eace-123">-ResourceGroupName</span></span>
<span data-ttu-id="6eace-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6eace-124">The name of the resource group.</span></span>
<span data-ttu-id="6eace-125">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6eace-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eace-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6eace-126">-SubscriptionId</span></span>
<span data-ttu-id="6eace-127">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6eace-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eace-128">-Címke</span><span class="sxs-lookup"><span data-stu-id="6eace-128">-Tag</span></span>
<span data-ttu-id="6eace-129">frissítendő Címkék</span><span class="sxs-lookup"><span data-stu-id="6eace-129">tags to be updated</span></span>

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

### <span data-ttu-id="6eace-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6eace-130">-Confirm</span></span>
<span data-ttu-id="6eace-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6eace-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eace-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eace-132">-WhatIf</span></span>
<span data-ttu-id="6eace-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6eace-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eace-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6eace-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eace-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eace-135">CommonParameters</span></span>
<span data-ttu-id="6eace-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6eace-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eace-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6eace-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eace-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eace-138">INPUTS</span></span>

### <span data-ttu-id="6eace-139">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="6eace-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="6eace-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6eace-140">OUTPUTS</span></span>

### <span data-ttu-id="6eace-141">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="6eace-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="6eace-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6eace-142">NOTES</span></span>

<span data-ttu-id="6eace-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="6eace-143">ALIASES</span></span>

<span data-ttu-id="6eace-144">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="6eace-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6eace-145">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6eace-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6eace-146">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6eace-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6eace-147">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6eace-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6eace-148">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="6eace-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="6eace-149">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="6eace-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="6eace-150">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="6eace-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="6eace-151">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="6eace-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="6eace-152">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6eace-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6eace-153">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6eace-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6eace-154">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="6eace-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="6eace-155">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="6eace-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="6eace-156">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6eace-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6eace-157">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="6eace-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="6eace-158">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="6eace-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="6eace-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6eace-159">RELATED LINKS</span></span>

