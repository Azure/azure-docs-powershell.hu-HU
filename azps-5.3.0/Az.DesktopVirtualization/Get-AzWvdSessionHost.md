---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 462f49884a7e38ea6808b594b091a6cca94c4e5e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469933"
---
# <span data-ttu-id="b7cf0-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="b7cf0-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="b7cf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cf0-103">Munkamenetgazda lekérte.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-103">Get a session host.</span></span>

## <span data-ttu-id="b7cf0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7cf0-104">SYNTAX</span></span>

### <span data-ttu-id="b7cf0-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7cf0-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7cf0-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="b7cf0-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7cf0-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7cf0-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7cf0-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7cf0-108">DESCRIPTION</span></span>
<span data-ttu-id="b7cf0-109">Munkamenetgazda lekérte.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-109">Get a session host.</span></span>

## <span data-ttu-id="b7cf0-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7cf0-110">EXAMPLES</span></span>

### <span data-ttu-id="b7cf0-111">1. példa: Windows Virtual Desktop SessionHost lekért név szerint</span><span class="sxs-lookup"><span data-stu-id="b7cf0-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="b7cf0-112">Ez a parancs egy Windows Virtual Desktop SessionHost-t kap egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="b7cf0-113">2. példa: Windows Virtual Desktop SessionHosts list</span><span class="sxs-lookup"><span data-stu-id="b7cf0-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="b7cf0-114">Ez a parancs felsorolja a Windows virtuális asztali SessionHosts-t egy gazdakészletben.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="b7cf0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7cf0-115">PARAMETERS</span></span>

### <span data-ttu-id="b7cf0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cf0-116">-DefaultProfile</span></span>
<span data-ttu-id="b7cf0-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7cf0-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b7cf0-118">-HostPoolName</span></span>
<span data-ttu-id="b7cf0-119">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="b7cf0-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b7cf0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7cf0-120">-InputObject</span></span>
<span data-ttu-id="b7cf0-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7cf0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b7cf0-122">-Name</span></span>
<span data-ttu-id="b7cf0-123">A munkamenetgazda neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="b7cf0-123">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7cf0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cf0-124">-ResourceGroupName</span></span>
<span data-ttu-id="b7cf0-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-125">The name of the resource group.</span></span>
<span data-ttu-id="b7cf0-126">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b7cf0-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b7cf0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7cf0-127">-SubscriptionId</span></span>
<span data-ttu-id="b7cf0-128">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-128">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7cf0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cf0-129">CommonParameters</span></span>
<span data-ttu-id="b7cf0-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cf0-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7cf0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cf0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7cf0-132">INPUTS</span></span>

### <span data-ttu-id="b7cf0-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b7cf0-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b7cf0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7cf0-134">OUTPUTS</span></span>

### <span data-ttu-id="b7cf0-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span><span class="sxs-lookup"><span data-stu-id="b7cf0-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.ISessionHost</span></span>

## <span data-ttu-id="b7cf0-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7cf0-136">NOTES</span></span>

<span data-ttu-id="b7cf0-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b7cf0-137">ALIASES</span></span>

<span data-ttu-id="b7cf0-138">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b7cf0-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7cf0-139">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7cf0-140">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7cf0-141">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b7cf0-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7cf0-142">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b7cf0-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b7cf0-143">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="b7cf0-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b7cf0-144">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="b7cf0-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b7cf0-145">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="b7cf0-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b7cf0-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b7cf0-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7cf0-147">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="b7cf0-147">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b7cf0-148">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b7cf0-149">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b7cf0-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b7cf0-150">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="b7cf0-150">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b7cf0-151">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b7cf0-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b7cf0-152">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="b7cf0-152">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b7cf0-153">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="b7cf0-153">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b7cf0-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7cf0-154">RELATED LINKS</span></span>

