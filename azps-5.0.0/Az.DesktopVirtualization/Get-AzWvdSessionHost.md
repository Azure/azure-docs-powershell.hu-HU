---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdSessionHost.md
ms.openlocfilehash: 94f4c5ad9c401c429c9ef2f2f1c146f83a407196
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297059"
---
# <span data-ttu-id="d2cad-101">Get-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="d2cad-101">Get-AzWvdSessionHost</span></span>

## <span data-ttu-id="d2cad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2cad-102">SYNOPSIS</span></span>
<span data-ttu-id="d2cad-103">Szerezzen be egy munkamenet-állomást.</span><span class="sxs-lookup"><span data-stu-id="d2cad-103">Get a session host.</span></span>

## <span data-ttu-id="d2cad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2cad-104">SYNTAX</span></span>

### <span data-ttu-id="d2cad-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2cad-105">List (Default)</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d2cad-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="d2cad-106">Get</span></span>
```
Get-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d2cad-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2cad-107">GetViaIdentity</span></span>
```
Get-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2cad-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2cad-108">DESCRIPTION</span></span>
<span data-ttu-id="d2cad-109">Szerezzen be egy munkamenet-állomást.</span><span class="sxs-lookup"><span data-stu-id="d2cad-109">Get a session host.</span></span>

## <span data-ttu-id="d2cad-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d2cad-110">EXAMPLES</span></span>

### <span data-ttu-id="d2cad-111">Példa 1: a Windows virtuális asztali SessionHost beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="d2cad-111">Example 1: Get a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="d2cad-112">Ez a parancs beolvassa a Windows virtuális asztali SessionHost egy alkalmazáskészletben.</span><span class="sxs-lookup"><span data-stu-id="d2cad-112">This command gets a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

### <span data-ttu-id="d2cad-113">2. példa: a Windows virtuális asztali SessionHosts listája</span><span class="sxs-lookup"><span data-stu-id="d2cad-113">Example 2: List Windows Virtual Desktop SessionHosts</span></span>
```powershell
PS C:\> Get-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

Name                                               Type
----                                               ----
HostPoolName/SessionHostName1 Microsoft.DesktopVirtualization/hostpools/sessionhosts
HostPoolName/SessionHostName2 Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="d2cad-114">Ez a parancs felsorolja a Windows virtuális asztali SessionHosts egy alkalmazáskészletben.</span><span class="sxs-lookup"><span data-stu-id="d2cad-114">This command lists a Windows Virtual Desktop SessionHosts in a Host Pool.</span></span>

## <span data-ttu-id="d2cad-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2cad-115">PARAMETERS</span></span>

### <span data-ttu-id="d2cad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2cad-116">-DefaultProfile</span></span>
<span data-ttu-id="d2cad-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2cad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2cad-118">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d2cad-118">-HostPoolName</span></span>
<span data-ttu-id="d2cad-119">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="d2cad-119">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d2cad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2cad-120">-InputObject</span></span>
<span data-ttu-id="d2cad-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d2cad-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2cad-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d2cad-122">-Name</span></span>
<span data-ttu-id="d2cad-123">A megadott alkalmazáskészleten belüli munkamenet-állomás neve</span><span class="sxs-lookup"><span data-stu-id="d2cad-123">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="d2cad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2cad-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2cad-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d2cad-125">The name of the resource group.</span></span>
<span data-ttu-id="d2cad-126">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d2cad-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d2cad-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2cad-127">-SubscriptionId</span></span>
<span data-ttu-id="d2cad-128">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d2cad-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d2cad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2cad-129">CommonParameters</span></span>
<span data-ttu-id="d2cad-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2cad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2cad-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d2cad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2cad-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2cad-132">INPUTS</span></span>

### <span data-ttu-id="d2cad-133">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="d2cad-133">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d2cad-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2cad-134">OUTPUTS</span></span>

### <span data-ttu-id="d2cad-135">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. ISessionHost</span><span class="sxs-lookup"><span data-stu-id="d2cad-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="d2cad-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2cad-136">NOTES</span></span>

<span data-ttu-id="d2cad-137">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="d2cad-137">ALIASES</span></span>

<span data-ttu-id="d2cad-138">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="d2cad-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2cad-139">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="d2cad-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2cad-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="d2cad-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2cad-141">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="d2cad-141">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2cad-142">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="d2cad-142">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d2cad-143">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="d2cad-143">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d2cad-144">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="d2cad-144">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d2cad-145">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="d2cad-145">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d2cad-146">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="d2cad-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2cad-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d2cad-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d2cad-148">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="d2cad-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="d2cad-149">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="d2cad-149">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d2cad-150">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d2cad-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d2cad-151">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="d2cad-151">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d2cad-152">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="d2cad-152">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="d2cad-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2cad-153">RELATED LINKS</span></span>

