---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184282"
---
# <span data-ttu-id="f5e4e-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="f5e4e-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="f5e4e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f5e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e4e-103">Megkapja az irányítópultot.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="f5e4e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f5e4e-104">SYNTAX</span></span>

### <span data-ttu-id="f5e4e-105">Lista1 (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f5e4e-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5e4e-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="f5e4e-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5e4e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f5e4e-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f5e4e-108">Lista</span><span class="sxs-lookup"><span data-stu-id="f5e4e-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f5e4e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f5e4e-109">DESCRIPTION</span></span>
<span data-ttu-id="f5e4e-110">Megkapja az irányítópultot.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="f5e4e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f5e4e-111">EXAMPLES</span></span>

### <span data-ttu-id="f5e4e-112">1. példa: az előfizetésben szereplő összes irányítópult listázása</span><span class="sxs-lookup"><span data-stu-id="f5e4e-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="f5e4e-113">Az összes irányítópult listázása az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="f5e4e-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="f5e4e-114">2. példa: egyetlen portál adatainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="f5e4e-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="f5e4e-115">Egyetlen irányítópult részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="f5e4e-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="f5e4e-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f5e4e-116">PARAMETERS</span></span>

### <span data-ttu-id="f5e4e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e4e-117">-DefaultProfile</span></span>
<span data-ttu-id="f5e4e-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e4e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5e4e-119">-InputObject</span></span>
<span data-ttu-id="f5e4e-120">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5e4e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f5e4e-121">-Name</span></span>
<span data-ttu-id="f5e4e-122">Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e4e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e4e-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5e4e-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="f5e4e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5e4e-125">-SubscriptionId</span></span>
<span data-ttu-id="f5e4e-126">Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-126">The Azure subscription ID.</span></span>
<span data-ttu-id="f5e4e-127">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="f5e4e-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="f5e4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e4e-128">CommonParameters</span></span>
<span data-ttu-id="f5e4e-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f5e4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e4e-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e4e-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5e4e-131">INPUTS</span></span>

### <span data-ttu-id="f5e4e-132">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="f5e4e-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="f5e4e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f5e4e-133">OUTPUTS</span></span>

### <span data-ttu-id="f5e4e-134">Microsoft. Azure. PowerShell. parancsmagok. Portal. models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="f5e4e-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="f5e4e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f5e4e-135">NOTES</span></span>

<span data-ttu-id="f5e4e-136">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="f5e4e-136">ALIASES</span></span>

<span data-ttu-id="f5e4e-137">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="f5e4e-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5e4e-138">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5e4e-139">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5e4e-140">INPUTOBJECT <IPortalIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="f5e4e-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5e4e-141">`[DashboardName <String>]`: Az irányítópult neve.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="f5e4e-142">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="f5e4e-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5e4e-143">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f5e4e-144">`[SubscriptionId <String>]`: Az Azure-előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f5e4e-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="f5e4e-145">Ez egy GUID formátumú karakterlánc (például 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="f5e4e-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="f5e4e-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f5e4e-146">RELATED LINKS</span></span>

