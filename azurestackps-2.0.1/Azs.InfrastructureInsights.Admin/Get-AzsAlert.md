---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94015298"
---
# <span data-ttu-id="0d306-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="0d306-101">Get-AzsAlert</span></span>

## <span data-ttu-id="0d306-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0d306-102">SYNOPSIS</span></span>
<span data-ttu-id="0d306-103">A kért riasztást számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0d306-103">Returns the requested alert.</span></span>

## <span data-ttu-id="0d306-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0d306-104">SYNTAX</span></span>

### <span data-ttu-id="0d306-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0d306-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d306-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="0d306-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0d306-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d306-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d306-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0d306-108">DESCRIPTION</span></span>
<span data-ttu-id="0d306-109">A kért riasztást számítja ki.</span><span class="sxs-lookup"><span data-stu-id="0d306-109">Returns the requested alert.</span></span>

## <span data-ttu-id="0d306-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0d306-110">EXAMPLES</span></span>

### <span data-ttu-id="0d306-111">Példa 1:</span><span class="sxs-lookup"><span data-stu-id="0d306-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="0d306-112">Értesítés kérése név alapján</span><span class="sxs-lookup"><span data-stu-id="0d306-112">Get an alert by Name.</span></span>

### <span data-ttu-id="0d306-113">2. példa:</span><span class="sxs-lookup"><span data-stu-id="0d306-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="0d306-114">Az összes aktív riasztás beolvasása és a hiba és a cím megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="0d306-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="0d306-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0d306-115">PARAMETERS</span></span>

### <span data-ttu-id="0d306-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d306-116">-DefaultProfile</span></span>
<span data-ttu-id="0d306-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0d306-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d306-118">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="0d306-118">-Filter</span></span>
<span data-ttu-id="0d306-119">OData-szűrő paraméter</span><span class="sxs-lookup"><span data-stu-id="0d306-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="0d306-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d306-120">-InputObject</span></span>
<span data-ttu-id="0d306-121">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0d306-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0d306-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="0d306-122">-Location</span></span>
<span data-ttu-id="0d306-123">A régió neve</span><span class="sxs-lookup"><span data-stu-id="0d306-123">Name of the region</span></span>

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

### <span data-ttu-id="0d306-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0d306-124">-Name</span></span>
<span data-ttu-id="0d306-125">A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="0d306-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0d306-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d306-126">-ResourceGroupName</span></span>
<span data-ttu-id="0d306-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d306-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="0d306-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d306-128">-SubscriptionId</span></span>
<span data-ttu-id="0d306-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="0d306-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0d306-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0d306-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0d306-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d306-131">CommonParameters</span></span>
<span data-ttu-id="0d306-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0d306-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d306-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0d306-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d306-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d306-134">INPUTS</span></span>

### <span data-ttu-id="0d306-135">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0d306-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="0d306-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0d306-136">OUTPUTS</span></span>

### <span data-ttu-id="0d306-137">Microsoft. Azure. PowerShell. parancsmagok. InfrastructureInsightsAdmin. modellek. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="0d306-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="0d306-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0d306-138">NOTES</span></span>

<span data-ttu-id="0d306-139">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="0d306-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d306-140">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="0d306-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0d306-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="0d306-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d306-142">`[AlertName <String>]`: A riasztás neve.</span><span class="sxs-lookup"><span data-stu-id="0d306-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="0d306-143">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="0d306-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d306-144">`[Location <String>]`: A régió neve</span><span class="sxs-lookup"><span data-stu-id="0d306-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="0d306-145">`[ResourceGroupName <String>]`: Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0d306-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="0d306-146">`[ResourceRegistrationId <String>]`: Erőforrás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="0d306-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="0d306-147">`[ServiceHealth <String>]`: Szolgáltatás állapota név.</span><span class="sxs-lookup"><span data-stu-id="0d306-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="0d306-148">`[ServiceRegistrationId <String>]`: Szolgáltatás-regisztrációs azonosító.</span><span class="sxs-lookup"><span data-stu-id="0d306-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="0d306-149">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="0d306-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0d306-150">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="0d306-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0d306-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0d306-151">RELATED LINKS</span></span>

