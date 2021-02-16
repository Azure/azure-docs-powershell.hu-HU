---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: 480c1d5517aa79ff7b3a0fa5dfa24f2ae6f4ae45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167747"
---
# <span data-ttu-id="32cdb-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="32cdb-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="32cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="32cdb-103">Állomáskészletet fog kapni.</span><span class="sxs-lookup"><span data-stu-id="32cdb-103">Get a host pool.</span></span>

## <span data-ttu-id="32cdb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="32cdb-104">SYNTAX</span></span>

### <span data-ttu-id="32cdb-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32cdb-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32cdb-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="32cdb-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="32cdb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="32cdb-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="32cdb-108">Lista</span><span class="sxs-lookup"><span data-stu-id="32cdb-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="32cdb-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="32cdb-109">DESCRIPTION</span></span>
<span data-ttu-id="32cdb-110">Állomáskészletet fog kapni.</span><span class="sxs-lookup"><span data-stu-id="32cdb-110">Get a host pool.</span></span>

## <span data-ttu-id="32cdb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="32cdb-111">EXAMPLES</span></span>

### <span data-ttu-id="32cdb-112">1. példa: Windows Virtual Desktop HostPool létrehozása név szerint</span><span class="sxs-lookup"><span data-stu-id="32cdb-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="32cdb-113">Ez a parancs egy Windows Virtual Desktop HostPool-t kap egy erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="32cdb-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="32cdb-114">2. példa: A Windows virtuális asztali hostpools listájának megjelenítése</span><span class="sxs-lookup"><span data-stu-id="32cdb-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="32cdb-115">Ez a parancs felsorolja az erőforráscsoportok windowsos virtuális asztali állomássorát.</span><span class="sxs-lookup"><span data-stu-id="32cdb-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="32cdb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32cdb-116">PARAMETERS</span></span>

### <span data-ttu-id="32cdb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cdb-117">-DefaultProfile</span></span>
<span data-ttu-id="32cdb-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32cdb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32cdb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32cdb-119">-InputObject</span></span>
<span data-ttu-id="32cdb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="32cdb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32cdb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="32cdb-121">-Name</span></span>
<span data-ttu-id="32cdb-122">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="32cdb-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cdb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32cdb-123">-ResourceGroupName</span></span>
<span data-ttu-id="32cdb-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="32cdb-124">The name of the resource group.</span></span>
<span data-ttu-id="32cdb-125">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="32cdb-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="32cdb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32cdb-126">-SubscriptionId</span></span>
<span data-ttu-id="32cdb-127">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="32cdb-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cdb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cdb-128">CommonParameters</span></span>
<span data-ttu-id="32cdb-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32cdb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cdb-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32cdb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cdb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32cdb-131">INPUTS</span></span>

### <span data-ttu-id="32cdb-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="32cdb-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="32cdb-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32cdb-133">OUTPUTS</span></span>

### <span data-ttu-id="32cdb-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.iHostPool</span><span class="sxs-lookup"><span data-stu-id="32cdb-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="32cdb-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="32cdb-135">NOTES</span></span>

<span data-ttu-id="32cdb-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="32cdb-136">ALIASES</span></span>

<span data-ttu-id="32cdb-137">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="32cdb-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32cdb-138">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="32cdb-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32cdb-139">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="32cdb-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32cdb-140">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="32cdb-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32cdb-141">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="32cdb-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="32cdb-142">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="32cdb-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="32cdb-143">`[DesktopName <String>]`: Az asztal neve a megadott asztali csoportban</span><span class="sxs-lookup"><span data-stu-id="32cdb-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="32cdb-144">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="32cdb-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="32cdb-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="32cdb-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32cdb-146">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="32cdb-146">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="32cdb-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="32cdb-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="32cdb-148">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="32cdb-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="32cdb-149">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="32cdb-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="32cdb-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="32cdb-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="32cdb-151">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="32cdb-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="32cdb-152">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="32cdb-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="32cdb-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32cdb-153">RELATED LINKS</span></span>

