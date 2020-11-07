---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842565"
---
# <span data-ttu-id="428ff-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="428ff-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="428ff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="428ff-102">SYNOPSIS</span></span>
<span data-ttu-id="428ff-103">A kért szolgáltatás állapotházirend-objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="428ff-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="428ff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="428ff-104">SYNTAX</span></span>

### <span data-ttu-id="428ff-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="428ff-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="428ff-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="428ff-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="428ff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="428ff-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="428ff-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="428ff-108">DESCRIPTION</span></span>
<span data-ttu-id="428ff-109">A kért szolgáltatás állapotházirend-objektum értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="428ff-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="428ff-110">Példák</span><span class="sxs-lookup"><span data-stu-id="428ff-110">EXAMPLES</span></span>

### <span data-ttu-id="428ff-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="428ff-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="428ff-112">Az egyes szolgáltatások állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="428ff-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="428ff-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="428ff-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="428ff-114">Egy szolgáltatás állapotát számítja ki.</span><span class="sxs-lookup"><span data-stu-id="428ff-114">Returns a service's health.</span></span>

## <span data-ttu-id="428ff-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="428ff-115">PARAMETERS</span></span>

### <span data-ttu-id="428ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="428ff-116">-DefaultProfile</span></span>
<span data-ttu-id="428ff-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="428ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="428ff-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="428ff-118">-Filter</span></span>
<span data-ttu-id="428ff-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="428ff-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="428ff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="428ff-120">-InputObject</span></span>
<span data-ttu-id="428ff-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="428ff-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="428ff-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="428ff-122">-Location</span></span>
<span data-ttu-id="428ff-123">A régió neve</span><span class="sxs-lookup"><span data-stu-id="428ff-123">Name of the region</span></span>

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

### <span data-ttu-id="428ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="428ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="428ff-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="428ff-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="428ff-126">-ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="428ff-126">-ServiceHealth</span></span>
<span data-ttu-id="428ff-127">Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="428ff-127">Service Health name.</span></span>

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

### <span data-ttu-id="428ff-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="428ff-128">-SubscriptionId</span></span>
<span data-ttu-id="428ff-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="428ff-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="428ff-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="428ff-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="428ff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="428ff-131">CommonParameters</span></span>
<span data-ttu-id="428ff-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="428ff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="428ff-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="428ff-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="428ff-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="428ff-134">INPUTS</span></span>

### <span data-ttu-id="428ff-135">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="428ff-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="428ff-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="428ff-136">OUTPUTS</span></span>

### <span data-ttu-id="428ff-137">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. modellek. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="428ff-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="428ff-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="428ff-138">NOTES</span></span>

<span data-ttu-id="428ff-139">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="428ff-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="428ff-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="428ff-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="428ff-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="428ff-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="428ff-142">`[AlertName <String>]`: A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="428ff-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="428ff-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="428ff-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="428ff-144">`[Location <String>]`: A régió neve</span><span class="sxs-lookup"><span data-stu-id="428ff-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="428ff-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="428ff-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="428ff-146">`[ResourceRegistrationId <String>]`: Erőforrás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="428ff-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="428ff-147">`[ServiceHealth <String>]`: Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="428ff-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="428ff-148">`[ServiceRegistrationId <String>]`: Szolgáltatás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="428ff-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="428ff-149">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="428ff-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="428ff-150">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="428ff-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="428ff-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="428ff-151">RELATED LINKS</span></span>

