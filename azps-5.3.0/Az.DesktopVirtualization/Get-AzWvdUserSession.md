---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 8dde4305003b97bd186a4601106a93e6f471edf4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469929"
---
# <span data-ttu-id="b59b6-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="b59b6-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="b59b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b59b6-102">SYNOPSIS</span></span>
<span data-ttu-id="b59b6-103">Felhasználói Session-et kap.</span><span class="sxs-lookup"><span data-stu-id="b59b6-103">Get a userSession.</span></span>

## <span data-ttu-id="b59b6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b59b6-104">SYNTAX</span></span>

### <span data-ttu-id="b59b6-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b59b6-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b59b6-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="b59b6-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b59b6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b59b6-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b59b6-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="b59b6-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b59b6-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b59b6-109">DESCRIPTION</span></span>
<span data-ttu-id="b59b6-110">Felhasználói Session-et kap.</span><span class="sxs-lookup"><span data-stu-id="b59b6-110">Get a userSession.</span></span>

## <span data-ttu-id="b59b6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b59b6-111">EXAMPLES</span></span>

### <span data-ttu-id="b59b6-112">1. példa: Windows virtuális asztali felhasználóhoz jut név szerint</span><span class="sxs-lookup"><span data-stu-id="b59b6-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="b59b6-113">Ez a parancs egy Windows virtuális asztali felhasználóSession-t kap egy munkamenetgazdában.</span><span class="sxs-lookup"><span data-stu-id="b59b6-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="b59b6-114">2. példa: A Windows virtuális asztali felhasználói felületének felsorolása</span><span class="sxs-lookup"><span data-stu-id="b59b6-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="b59b6-115">Ez a parancs felsorolja a Windows virtuális asztali felhasználófelhasználói munkamenetgazda egy munkamenetgazdáit.</span><span class="sxs-lookup"><span data-stu-id="b59b6-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="b59b6-116">3. példa: A Windows virtuális asztal felhasználóinak listájának megjelenítése az állomáskészletben</span><span class="sxs-lookup"><span data-stu-id="b59b6-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="b59b6-117">Ez a parancs felsorolja egy windowsos virtuális asztali felhasználó-összetűnések listáját egy gazdakészlet munkamenetgazdáiban.</span><span class="sxs-lookup"><span data-stu-id="b59b6-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="b59b6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b59b6-118">PARAMETERS</span></span>

### <span data-ttu-id="b59b6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b59b6-119">-DefaultProfile</span></span>
<span data-ttu-id="b59b6-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b59b6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b59b6-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="b59b6-121">-Filter</span></span>
<span data-ttu-id="b59b6-122">OData-szűrőkifejezés.</span><span class="sxs-lookup"><span data-stu-id="b59b6-122">OData filter expression.</span></span>
<span data-ttu-id="b59b6-123">A szűrés érvényes tulajdonságai a userprincipalname és a sessionstate.</span><span class="sxs-lookup"><span data-stu-id="b59b6-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59b6-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b59b6-124">-HostPoolName</span></span>
<span data-ttu-id="b59b6-125">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="b59b6-125">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59b6-126">-Id</span><span class="sxs-lookup"><span data-stu-id="b59b6-126">-Id</span></span>
<span data-ttu-id="b59b6-127">A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="b59b6-127">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59b6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b59b6-128">-InputObject</span></span>
<span data-ttu-id="b59b6-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b59b6-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b59b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b59b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="b59b6-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b59b6-131">The name of the resource group.</span></span>
<span data-ttu-id="b59b6-132">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b59b6-132">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59b6-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="b59b6-133">-SessionHostName</span></span>
<span data-ttu-id="b59b6-134">A munkamenetgazda neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="b59b6-134">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b59b6-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b59b6-135">-SubscriptionId</span></span>
<span data-ttu-id="b59b6-136">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b59b6-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b59b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b59b6-137">CommonParameters</span></span>
<span data-ttu-id="b59b6-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b59b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b59b6-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b59b6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b59b6-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b59b6-140">INPUTS</span></span>

### <span data-ttu-id="b59b6-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b59b6-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b59b6-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b59b6-142">OUTPUTS</span></span>

### <span data-ttu-id="b59b6-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="b59b6-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IUserSession</span></span>

## <span data-ttu-id="b59b6-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b59b6-144">NOTES</span></span>

<span data-ttu-id="b59b6-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b59b6-145">ALIASES</span></span>

<span data-ttu-id="b59b6-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="b59b6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b59b6-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="b59b6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b59b6-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b59b6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b59b6-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="b59b6-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b59b6-150">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="b59b6-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b59b6-151">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="b59b6-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b59b6-152">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="b59b6-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b59b6-153">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="b59b6-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b59b6-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b59b6-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b59b6-155">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="b59b6-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b59b6-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b59b6-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b59b6-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="b59b6-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="b59b6-158">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="b59b6-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b59b6-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b59b6-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b59b6-160">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="b59b6-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b59b6-161">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="b59b6-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b59b6-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b59b6-162">RELATED LINKS</span></span>

