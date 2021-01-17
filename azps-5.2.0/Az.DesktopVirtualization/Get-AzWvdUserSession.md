---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: 0b0a044b9521236c3a29e7deffa15840b6d039ef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369458"
---
# <span data-ttu-id="e5545-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="e5545-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="e5545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5545-102">SYNOPSIS</span></span>
<span data-ttu-id="e5545-103">Felhasználói Session-et kap.</span><span class="sxs-lookup"><span data-stu-id="e5545-103">Get a userSession.</span></span>

## <span data-ttu-id="e5545-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e5545-104">SYNTAX</span></span>

### <span data-ttu-id="e5545-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e5545-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e5545-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="e5545-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e5545-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e5545-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5545-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="e5545-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e5545-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e5545-109">DESCRIPTION</span></span>
<span data-ttu-id="e5545-110">Felhasználói Session-et kap.</span><span class="sxs-lookup"><span data-stu-id="e5545-110">Get a userSession.</span></span>

## <span data-ttu-id="e5545-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e5545-111">EXAMPLES</span></span>

### <span data-ttu-id="e5545-112">1. példa: Windows virtuális asztali felhasználóhoz jut név szerint</span><span class="sxs-lookup"><span data-stu-id="e5545-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="e5545-113">Ez a parancs egy Windows virtuális asztali felhasználóSession-t kap egy munkamenetgazdában.</span><span class="sxs-lookup"><span data-stu-id="e5545-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="e5545-114">2. példa: A Windows virtuális asztali felhasználói felületének felsorolása</span><span class="sxs-lookup"><span data-stu-id="e5545-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="e5545-115">Ez a parancs felsorolja a Windows virtuális asztali felhasználófelhasználói munkamenetgazda egy munkamenetgazdáit.</span><span class="sxs-lookup"><span data-stu-id="e5545-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="e5545-116">3. példa: A Windows virtuális asztal felhasználóinak listájának megjelenítése az állomáskészletben</span><span class="sxs-lookup"><span data-stu-id="e5545-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="e5545-117">Ez a parancs felsorolja egy windowsos virtuális asztali felhasználó-összetűnések listáját egy gazdakészlet munkamenetgazdáiban.</span><span class="sxs-lookup"><span data-stu-id="e5545-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="e5545-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5545-118">PARAMETERS</span></span>

### <span data-ttu-id="e5545-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5545-119">-DefaultProfile</span></span>
<span data-ttu-id="e5545-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5545-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5545-121">-Filter</span><span class="sxs-lookup"><span data-stu-id="e5545-121">-Filter</span></span>
<span data-ttu-id="e5545-122">OData-szűrőkifejezés.</span><span class="sxs-lookup"><span data-stu-id="e5545-122">OData filter expression.</span></span>
<span data-ttu-id="e5545-123">A szűrés érvényes tulajdonságai a userprincipalname és a sessionstate.</span><span class="sxs-lookup"><span data-stu-id="e5545-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="e5545-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="e5545-124">-HostPoolName</span></span>
<span data-ttu-id="e5545-125">A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="e5545-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="e5545-126">-Id</span><span class="sxs-lookup"><span data-stu-id="e5545-126">-Id</span></span>
<span data-ttu-id="e5545-127">A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="e5545-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="e5545-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5545-128">-InputObject</span></span>
<span data-ttu-id="e5545-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="e5545-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e5545-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5545-130">-ResourceGroupName</span></span>
<span data-ttu-id="e5545-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e5545-131">The name of the resource group.</span></span>
<span data-ttu-id="e5545-132">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e5545-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e5545-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="e5545-133">-SessionHostName</span></span>
<span data-ttu-id="e5545-134">A munkamenetgazda neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="e5545-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="e5545-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5545-135">-SubscriptionId</span></span>
<span data-ttu-id="e5545-136">A célként megcélzott előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e5545-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e5545-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5545-137">CommonParameters</span></span>
<span data-ttu-id="e5545-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5545-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5545-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5545-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5545-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5545-140">INPUTS</span></span>

### <span data-ttu-id="e5545-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="e5545-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="e5545-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5545-142">OUTPUTS</span></span>

### <span data-ttu-id="e5545-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IUserSession</span><span class="sxs-lookup"><span data-stu-id="e5545-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IUserSession</span></span>

## <span data-ttu-id="e5545-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e5545-144">NOTES</span></span>

<span data-ttu-id="e5545-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="e5545-145">ALIASES</span></span>

<span data-ttu-id="e5545-146">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="e5545-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e5545-147">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="e5545-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e5545-148">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e5545-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e5545-149">INPUTOBJECT: <IDesktopVirtualizationIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="e5545-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e5545-150">`[ApplicationGroupName <String>]`: Az alkalmazáscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e5545-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="e5545-151">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazáscsoporton belül</span><span class="sxs-lookup"><span data-stu-id="e5545-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="e5545-152">`[DesktopName <String>]`: A megadott asztali csoportban található asztal neve</span><span class="sxs-lookup"><span data-stu-id="e5545-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="e5545-153">`[HostPoolName <String>]`: A megadott erőforráscsoporton belüli állomáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="e5545-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="e5545-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="e5545-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e5545-155">`[MsixPackageFullName <String>]`: A megadott állomáspoolon belül az MSIX-csomag teljes neve verzióspecifikus csomag</span><span class="sxs-lookup"><span data-stu-id="e5545-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="e5545-156">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e5545-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e5545-157">A névben a kis- és</span><span class="sxs-lookup"><span data-stu-id="e5545-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="e5545-158">`[SessionHostName <String>]`: A munkamenet állomásának neve a megadott gazdakészleten belül</span><span class="sxs-lookup"><span data-stu-id="e5545-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="e5545-159">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e5545-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e5545-160">`[UserSessionId <String>]`: A megadott munkamenetgazda felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="e5545-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="e5545-161">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="e5545-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="e5545-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5545-162">RELATED LINKS</span></span>

