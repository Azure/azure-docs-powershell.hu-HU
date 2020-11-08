---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdHostPool.md
ms.openlocfilehash: e04d13b96f36b96b2ae1c22f6f6e5b3c50b338f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182794"
---
# <span data-ttu-id="57332-101">Get-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="57332-101">Get-AzWvdHostPool</span></span>

## <span data-ttu-id="57332-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57332-102">SYNOPSIS</span></span>
<span data-ttu-id="57332-103">Beszerezhet egy alkalmazáskészletet.</span><span class="sxs-lookup"><span data-stu-id="57332-103">Get a host pool.</span></span>

## <span data-ttu-id="57332-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57332-104">SYNTAX</span></span>

### <span data-ttu-id="57332-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57332-105">List1 (Default)</span></span>
```
Get-AzWvdHostPool [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57332-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="57332-106">Get</span></span>
```
Get-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57332-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57332-107">GetViaIdentity</span></span>
```
Get-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="57332-108">Lista</span><span class="sxs-lookup"><span data-stu-id="57332-108">List</span></span>
```
Get-AzWvdHostPool -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="57332-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="57332-109">DESCRIPTION</span></span>
<span data-ttu-id="57332-110">Beszerezhet egy alkalmazáskészletet.</span><span class="sxs-lookup"><span data-stu-id="57332-110">Get a host pool.</span></span>

## <span data-ttu-id="57332-111">Példák</span><span class="sxs-lookup"><span data-stu-id="57332-111">EXAMPLES</span></span>

### <span data-ttu-id="57332-112">Példa 1: a Windows virtuális asztali HostPool beszerzése név szerint</span><span class="sxs-lookup"><span data-stu-id="57332-112">Example 1: Get a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="57332-113">Ez a parancs egy erőforráscsoport Windows virtuális asztali HostPool kap.</span><span class="sxs-lookup"><span data-stu-id="57332-113">This command gets a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="57332-114">2. példa: a Windows virtuális asztali HostPools listája</span><span class="sxs-lookup"><span data-stu-id="57332-114">Example 2: List Windows Virtual Desktop HostPools</span></span>
```powershell
PS C:\> Get-AzWvdHostPool -ResourceGroupName ResourceGroupName

Location   Name          Type
--------   ----          ----
eastus     HostPoolName1 Microsoft.DesktopVirtualization/hostpools
eastus     HostPoolName2 Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="57332-115">Ez a parancs egy erőforráscsoport Windows virtuális asztali HostPools sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="57332-115">This command lists a Windows Virtual Desktop HostPools in a Resource Group.</span></span>

## <span data-ttu-id="57332-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57332-116">PARAMETERS</span></span>

### <span data-ttu-id="57332-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57332-117">-DefaultProfile</span></span>
<span data-ttu-id="57332-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57332-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57332-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57332-119">-InputObject</span></span>
<span data-ttu-id="57332-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="57332-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57332-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57332-121">-Name</span></span>
<span data-ttu-id="57332-122">A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="57332-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="57332-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57332-123">-ResourceGroupName</span></span>
<span data-ttu-id="57332-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="57332-124">The name of the resource group.</span></span>
<span data-ttu-id="57332-125">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="57332-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="57332-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57332-126">-SubscriptionId</span></span>
<span data-ttu-id="57332-127">A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="57332-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="57332-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57332-128">CommonParameters</span></span>
<span data-ttu-id="57332-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57332-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57332-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="57332-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57332-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57332-131">INPUTS</span></span>

### <span data-ttu-id="57332-132">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="57332-132">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="57332-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57332-133">OUTPUTS</span></span>

### <span data-ttu-id="57332-134">Microsoft. Azure. PowerShell. parancsmagok. DesktopVirtualization. modellek. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="57332-134">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="57332-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57332-135">NOTES</span></span>

<span data-ttu-id="57332-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="57332-136">ALIASES</span></span>

<span data-ttu-id="57332-137">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="57332-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57332-138">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="57332-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57332-139">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="57332-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57332-140">INPUTOBJECT <IDesktopVirtualizationIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="57332-140">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57332-141">`[ApplicationGroupName <String>]`: Az alkalmazás csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="57332-141">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="57332-142">`[ApplicationName <String>]`: Az alkalmazás neve a megadott alkalmazásobjektum-csoporton belül</span><span class="sxs-lookup"><span data-stu-id="57332-142">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="57332-143">`[DesktopName <String>]`: A megadott asztali csoportban lévő asztal neve</span><span class="sxs-lookup"><span data-stu-id="57332-143">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="57332-144">`[HostPoolName <String>]`: A megadott erőforráscsoporthoz tartozó alkalmazáskészlet neve</span><span class="sxs-lookup"><span data-stu-id="57332-144">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="57332-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="57332-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57332-146">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="57332-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="57332-147">A név a kis-és nagybetűk megkülönböztetésére szolgál.</span><span class="sxs-lookup"><span data-stu-id="57332-147">The name is case insensitive.</span></span>
  - <span data-ttu-id="57332-148">`[SessionHostName <String>]`: A megadott alkalmazáskészleten belüli Munkamenetcímtár neve</span><span class="sxs-lookup"><span data-stu-id="57332-148">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="57332-149">`[SubscriptionId <String>]`: A cél-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="57332-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="57332-150">`[UserSessionId <String>]`: A megadott Munkamenetcímtár felhasználói munkamenetének neve</span><span class="sxs-lookup"><span data-stu-id="57332-150">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="57332-151">`[WorkspaceName <String>]`: A munkaterület neve</span><span class="sxs-lookup"><span data-stu-id="57332-151">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="57332-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57332-152">RELATED LINKS</span></span>

