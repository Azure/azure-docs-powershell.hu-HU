---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016706"
---
# <span data-ttu-id="8857d-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="8857d-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="8857d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8857d-102">SYNOPSIS</span></span>
<span data-ttu-id="8857d-103">Az adott erőforráshoz szükséges egészségügyi információkat számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8857d-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="8857d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8857d-104">SYNTAX</span></span>

### <span data-ttu-id="8857d-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8857d-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8857d-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="8857d-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8857d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8857d-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8857d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8857d-108">DESCRIPTION</span></span>
<span data-ttu-id="8857d-109">Az adott erőforráshoz szükséges egészségügyi információkat számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8857d-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="8857d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8857d-110">EXAMPLES</span></span>

### <span data-ttu-id="8857d-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="8857d-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="8857d-112">A szolgáltatás alatti erőforrások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8857d-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="8857d-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="8857d-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="8857d-114">Az a for Microsoft. Fabric. admin elemhez tartozó állapotot számítja ki.</span><span class="sxs-lookup"><span data-stu-id="8857d-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="8857d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8857d-115">PARAMETERS</span></span>

### <span data-ttu-id="8857d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8857d-116">-DefaultProfile</span></span>
<span data-ttu-id="8857d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8857d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8857d-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="8857d-118">-Filter</span></span>
<span data-ttu-id="8857d-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="8857d-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="8857d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8857d-120">-InputObject</span></span>
<span data-ttu-id="8857d-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8857d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8857d-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="8857d-122">-Location</span></span>
<span data-ttu-id="8857d-123">A régió neve</span><span class="sxs-lookup"><span data-stu-id="8857d-123">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8857d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8857d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8857d-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8857d-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8857d-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="8857d-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="8857d-127">Erőforrás-regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="8857d-127">Resource registration ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8857d-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="8857d-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="8857d-129">Szolgáltatás-regisztrációs azonosító</span><span class="sxs-lookup"><span data-stu-id="8857d-129">Service registration ID.</span></span>

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

### <span data-ttu-id="8857d-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8857d-130">-SubscriptionId</span></span>
<span data-ttu-id="8857d-131">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="8857d-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8857d-132">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8857d-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8857d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8857d-133">CommonParameters</span></span>
<span data-ttu-id="8857d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8857d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8857d-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8857d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8857d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8857d-136">INPUTS</span></span>

### <span data-ttu-id="8857d-137">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8857d-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="8857d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8857d-138">OUTPUTS</span></span>

### <span data-ttu-id="8857d-139">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. modellek. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="8857d-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="8857d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8857d-140">NOTES</span></span>

<span data-ttu-id="8857d-141">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="8857d-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8857d-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="8857d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8857d-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="8857d-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8857d-144">`[AlertName <String>]`: A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="8857d-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="8857d-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="8857d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8857d-146">`[Location <String>]`: A régió neve</span><span class="sxs-lookup"><span data-stu-id="8857d-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="8857d-147">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8857d-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8857d-148">`[ResourceRegistrationId <String>]`: Erőforrás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="8857d-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="8857d-149">`[ServiceHealth <String>]`: Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="8857d-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="8857d-150">`[ServiceRegistrationId <String>]`: Szolgáltatás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="8857d-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="8857d-151">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="8857d-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8857d-152">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="8857d-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8857d-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8857d-153">RELATED LINKS</span></span>

