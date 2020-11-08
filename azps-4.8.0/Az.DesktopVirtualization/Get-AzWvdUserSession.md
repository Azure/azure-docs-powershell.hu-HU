---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdUserSession.md
ms.openlocfilehash: eedf639ebf5c25ff9153072a337ea659b41a9e92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182261"
---
# <span data-ttu-id="cc18a-101">Get-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="cc18a-101">Get-AzWvdUserSession</span></span>

## <span data-ttu-id="cc18a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cc18a-102">SYNOPSIS</span></span>
<span data-ttu-id="cc18a-103">UserSession beszerzése</span><span class="sxs-lookup"><span data-stu-id="cc18a-103">Get a userSession.</span></span>

## <span data-ttu-id="cc18a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cc18a-104">SYNTAX</span></span>

### <span data-ttu-id="cc18a-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cc18a-105">List (Default)</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc18a-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="cc18a-106">Get</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cc18a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cc18a-107">GetViaIdentity</span></span>
```
Get-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc18a-108">Lista1</span><span class="sxs-lookup"><span data-stu-id="cc18a-108">List1</span></span>
```
Get-AzWvdUserSession -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cc18a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="cc18a-109">DESCRIPTION</span></span>
<span data-ttu-id="cc18a-110">UserSession beszerzése</span><span class="sxs-lookup"><span data-stu-id="cc18a-110">Get a userSession.</span></span>

## <span data-ttu-id="cc18a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cc18a-111">EXAMPLES</span></span>

### <span data-ttu-id="cc18a-112">Példa 1: a Windows virtuális asztali UserSession beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="cc18a-112">Example 1: Get a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="cc18a-113">Ez a parancs a Windows virtuális asztali UserSession a munkamenet-állomáson.</span><span class="sxs-lookup"><span data-stu-id="cc18a-113">This command gets a Windows Virtual Desktop UserSession in a Session Host.</span></span>

### <span data-ttu-id="cc18a-114">2. példa: a Windows virtuális asztali UserSessions listája</span><span class="sxs-lookup"><span data-stu-id="cc18a-114">Example 2: List Windows Virtual Desktop UserSessions</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="cc18a-115">Ez a parancs felsorolja a Windows virtuális asztali UserSessions a munkamenet-tárolóban.</span><span class="sxs-lookup"><span data-stu-id="cc18a-115">This command lists a Windows Virtual Desktop UserSessions in a Session Host.</span></span>

### <span data-ttu-id="cc18a-116">3. példa: a Windows virtuális asztali UserSessions listázása a Host Pool-ban</span><span class="sxs-lookup"><span data-stu-id="cc18a-116">Example 3: List Windows Virtual Desktop UserSessions in host pool</span></span>
```powershell
PS C:\> Get-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                           Type
----                           ----
HostPoolName/SessionHostName/2 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
HostPoolName/SessionHostName/3 Microsoft.DesktopVirtualization/hostpools/sessionhosts/usersessions
```

<span data-ttu-id="cc18a-117">Ez a parancs felsorolja a Windows virtuális asztali UserSessions egy állomás egy alkalmazáskészletében.</span><span class="sxs-lookup"><span data-stu-id="cc18a-117">This command lists a Windows Virtual Desktop UserSessions in a Session Host in a host pool.</span></span>

## <span data-ttu-id="cc18a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cc18a-118">PARAMETERS</span></span>

### <span data-ttu-id="cc18a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc18a-119">-DefaultProfile</span></span>
<span data-ttu-id="cc18a-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cc18a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc18a-121">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="cc18a-121">-Filter</span></span>
<span data-ttu-id="cc18a-122">OData-szűrési kifejezés</span><span class="sxs-lookup"><span data-stu-id="cc18a-122">OData filter expression.</span></span>
<span data-ttu-id="cc18a-123">A szűréshez érvényes tulajdonságok a userPrincipalName és a sessionstate.</span><span class="sxs-lookup"><span data-stu-id="cc18a-123">Valid properties for filtering are userprincipalname and sessionstate.</span></span>

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

### <span data-ttu-id="cc18a-124">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="cc18a-124">-HostPoolName</span></span>
<span data-ttu-id="cc18a-125">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="cc18a-125">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="cc18a-126">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="cc18a-126">-Id</span></span>
<span data-ttu-id="cc18a-127">A felhasználó munkamenetének neve a megadott munkamenet-állomáson belül</span><span class="sxs-lookup"><span data-stu-id="cc18a-127">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="cc18a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc18a-128">-InputObject</span></span>
<span data-ttu-id="cc18a-129">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc18a-129">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cc18a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc18a-130">-ResourceGroupName</span></span>
<span data-ttu-id="cc18a-131">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cc18a-131">The name of the resource group.</span></span>
<span data-ttu-id="cc18a-132">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="cc18a-132">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cc18a-133">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="cc18a-133">-SessionHostName</span></span>
<span data-ttu-id="cc18a-134">A megadott alkalmazáskészleten belüli munkamenet-állomás neve</span><span class="sxs-lookup"><span data-stu-id="cc18a-134">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="cc18a-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc18a-135">-SubscriptionId</span></span>
<span data-ttu-id="cc18a-136">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cc18a-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cc18a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc18a-137">CommonParameters</span></span>
<span data-ttu-id="cc18a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cc18a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc18a-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cc18a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc18a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc18a-140">INPUTS</span></span>

### <span data-ttu-id="cc18a-141">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cc18a-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cc18a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc18a-142">OUTPUTS</span></span>

### <span data-ttu-id="cc18a-143">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IUserSession</span><span class="sxs-lookup"><span data-stu-id="cc18a-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IUserSession</span></span>

## <span data-ttu-id="cc18a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cc18a-144">NOTES</span></span>

<span data-ttu-id="cc18a-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cc18a-145">ALIASES</span></span>

<span data-ttu-id="cc18a-146">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="cc18a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc18a-147">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="cc18a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc18a-148">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="cc18a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc18a-149">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="cc18a-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc18a-150">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="cc18a-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cc18a-151">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="cc18a-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cc18a-152">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="cc18a-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cc18a-153">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="cc18a-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cc18a-154">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="cc18a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc18a-155">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cc18a-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cc18a-156">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="cc18a-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="cc18a-157">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="cc18a-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cc18a-158">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cc18a-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cc18a-159">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="cc18a-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cc18a-160">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="cc18a-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cc18a-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc18a-161">RELATED LINKS</span></span>

