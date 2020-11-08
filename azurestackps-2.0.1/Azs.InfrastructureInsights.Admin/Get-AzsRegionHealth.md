---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015288"
---
# <span data-ttu-id="6ab65-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="6ab65-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="6ab65-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6ab65-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab65-103">Egy régió kívánt állapotának értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6ab65-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="6ab65-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6ab65-104">SYNTAX</span></span>

### <span data-ttu-id="6ab65-105">Get (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6ab65-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ab65-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ab65-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab65-107">Lista</span><span class="sxs-lookup"><span data-stu-id="6ab65-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6ab65-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6ab65-108">DESCRIPTION</span></span>
<span data-ttu-id="6ab65-109">Egy régió kívánt állapotának értékét számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6ab65-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="6ab65-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6ab65-110">EXAMPLES</span></span>

### <span data-ttu-id="6ab65-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="6ab65-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="6ab65-112">A tartomány állapotának listáját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="6ab65-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="6ab65-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6ab65-113">PARAMETERS</span></span>

### <span data-ttu-id="6ab65-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab65-114">-DefaultProfile</span></span>
<span data-ttu-id="6ab65-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6ab65-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab65-116">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="6ab65-116">-Filter</span></span>
<span data-ttu-id="6ab65-117">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="6ab65-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="6ab65-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ab65-118">-InputObject</span></span>
<span data-ttu-id="6ab65-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ab65-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6ab65-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="6ab65-120">-Location</span></span>
<span data-ttu-id="6ab65-121">A régió neve</span><span class="sxs-lookup"><span data-stu-id="6ab65-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6ab65-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab65-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ab65-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6ab65-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ab65-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ab65-124">-SubscriptionId</span></span>
<span data-ttu-id="6ab65-125">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="6ab65-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6ab65-126">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6ab65-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6ab65-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab65-127">CommonParameters</span></span>
<span data-ttu-id="6ab65-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6ab65-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab65-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6ab65-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab65-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ab65-130">INPUTS</span></span>

### <span data-ttu-id="6ab65-131">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="6ab65-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="6ab65-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6ab65-132">OUTPUTS</span></span>

### <span data-ttu-id="6ab65-133">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. modellek. Api20160501. IRegionHealth</span><span class="sxs-lookup"><span data-stu-id="6ab65-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="6ab65-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6ab65-134">NOTES</span></span>

<span data-ttu-id="6ab65-135">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="6ab65-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ab65-136">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="6ab65-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6ab65-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="6ab65-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ab65-138">`[AlertName <String>]`: A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="6ab65-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="6ab65-139">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="6ab65-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ab65-140">`[Location <String>]`: A régió neve</span><span class="sxs-lookup"><span data-stu-id="6ab65-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="6ab65-141">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6ab65-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6ab65-142">`[ResourceRegistrationId <String>]`: Erőforrás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="6ab65-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="6ab65-143">`[ServiceHealth <String>]`: Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="6ab65-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="6ab65-144">`[ServiceRegistrationId <String>]`: Szolgáltatás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="6ab65-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="6ab65-145">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="6ab65-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6ab65-146">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="6ab65-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6ab65-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6ab65-147">RELATED LINKS</span></span>

