---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016733"
---
# <span data-ttu-id="b414c-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="b414c-101">Get-AzsLocation</span></span>

## <span data-ttu-id="b414c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b414c-102">SYNOPSIS</span></span>
<span data-ttu-id="b414c-103">A megadott hely beszerzése</span><span class="sxs-lookup"><span data-stu-id="b414c-103">Get the specified location.</span></span>

## <span data-ttu-id="b414c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b414c-104">SYNTAX</span></span>

### <span data-ttu-id="b414c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b414c-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b414c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b414c-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b414c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b414c-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b414c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b414c-108">DESCRIPTION</span></span>
<span data-ttu-id="b414c-109">A megadott hely beszerzése</span><span class="sxs-lookup"><span data-stu-id="b414c-109">Get the specified location.</span></span>

## <span data-ttu-id="b414c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b414c-110">EXAMPLES</span></span>

### <span data-ttu-id="b414c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b414c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="b414c-112">A AzureStack-helyek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="b414c-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="b414c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b414c-113">PARAMETERS</span></span>

### <span data-ttu-id="b414c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b414c-114">-DefaultProfile</span></span>
<span data-ttu-id="b414c-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b414c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b414c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b414c-116">-InputObject</span></span>
<span data-ttu-id="b414c-117">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b414c-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b414c-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b414c-118">-Name</span></span>
<span data-ttu-id="b414c-119">A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="b414c-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b414c-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b414c-120">-SubscriptionId</span></span>
<span data-ttu-id="b414c-121">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b414c-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b414c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b414c-122">CommonParameters</span></span>
<span data-ttu-id="b414c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b414c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b414c-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b414c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b414c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b414c-125">INPUTS</span></span>

### <span data-ttu-id="b414c-126">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b414c-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b414c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b414c-127">OUTPUTS</span></span>

### <span data-ttu-id="b414c-128">Microsoft. Azure. PowerShell. parancsmagok. SubscriptionsAdmin. modellek. Api20151101. ILocation</span><span class="sxs-lookup"><span data-stu-id="b414c-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="b414c-129">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="b414c-129">ALIASES</span></span>

## <span data-ttu-id="b414c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b414c-130">NOTES</span></span>

<span data-ttu-id="b414c-131">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b414c-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b414c-132">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b414c-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b414c-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b414c-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b414c-134">`[DelegatedProvider <String>]`: DelegatedProvider-azonosító.</span><span class="sxs-lookup"><span data-stu-id="b414c-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b414c-135">`[DelegatedProviderSubscriptionId <String>]`: Delegált szolgáltatói előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="b414c-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b414c-136">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b414c-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b414c-137">`[Location <String>]`: A AzureStack helye.</span><span class="sxs-lookup"><span data-stu-id="b414c-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b414c-138">`[ManifestName <String>]`: A jegyzékfájl neve.</span><span class="sxs-lookup"><span data-stu-id="b414c-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b414c-139">`[Offer <String>]`: Ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="b414c-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b414c-140">`[OfferDelegationName <String>]`: Az ajánlati meghatalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="b414c-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b414c-141">`[OperationsStatusName <String>]`: A művelet állapota név.</span><span class="sxs-lookup"><span data-stu-id="b414c-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b414c-142">`[Plan <String>]`: A terv neve.</span><span class="sxs-lookup"><span data-stu-id="b414c-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b414c-143">`[PlanAcquisitionId <String>]`: A terv beszerzésének azonosítója</span><span class="sxs-lookup"><span data-stu-id="b414c-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b414c-144">`[Quota <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="b414c-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b414c-145">`[ResourceGroupName <String>]`: Az erőforrás az erőforrás csoportban található.</span><span class="sxs-lookup"><span data-stu-id="b414c-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b414c-146">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést. Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b414c-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b414c-147">`[TargetSubscriptionId <String>]`: A cél-előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="b414c-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b414c-148">`[Tenant <String>]`: Címtár-bérlői név.</span><span class="sxs-lookup"><span data-stu-id="b414c-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b414c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b414c-149">RELATED LINKS</span></span>

