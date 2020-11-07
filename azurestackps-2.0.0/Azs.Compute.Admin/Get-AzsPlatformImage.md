---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844877"
---
# <span data-ttu-id="b6f15-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b6f15-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="b6f15-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b6f15-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f15-103">A megfelelő platformot jeleníti meg, amely megfelel a Publisher, az ajánlat, a SKU és a verzió típusának.</span><span class="sxs-lookup"><span data-stu-id="b6f15-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="b6f15-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b6f15-104">SYNTAX</span></span>

### <span data-ttu-id="b6f15-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b6f15-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b6f15-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="b6f15-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b6f15-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b6f15-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b6f15-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="b6f15-108">DESCRIPTION</span></span>
<span data-ttu-id="b6f15-109">A megfelelő platformot jeleníti meg, amely megfelel a Publisher, az ajánlat, a SKU és a verzió típusának.</span><span class="sxs-lookup"><span data-stu-id="b6f15-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="b6f15-110">Példák</span><span class="sxs-lookup"><span data-stu-id="b6f15-110">EXAMPLES</span></span>

### <span data-ttu-id="b6f15-111">Példa 1: az összes platform-kép beolvasása</span><span class="sxs-lookup"><span data-stu-id="b6f15-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="b6f15-112">Az összes paraméter üres kihagyása a platform összes képéről</span><span class="sxs-lookup"><span data-stu-id="b6f15-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="b6f15-113">2. példa: adott platform képének beszerzése</span><span class="sxs-lookup"><span data-stu-id="b6f15-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="b6f15-114">Az ajánlat, a Publisher, a hely, a SKU és a verzió megadásával lekérheti a platform képét.</span><span class="sxs-lookup"><span data-stu-id="b6f15-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="b6f15-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b6f15-115">PARAMETERS</span></span>

### <span data-ttu-id="b6f15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f15-116">-DefaultProfile</span></span>
<span data-ttu-id="b6f15-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6f15-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f15-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6f15-118">-InputObject</span></span>
<span data-ttu-id="b6f15-119">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6f15-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b6f15-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="b6f15-120">-Location</span></span>
<span data-ttu-id="b6f15-121">Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b6f15-121">Location of the resource.</span></span>

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

### <span data-ttu-id="b6f15-122">-Ajánlat</span><span class="sxs-lookup"><span data-stu-id="b6f15-122">-Offer</span></span>
<span data-ttu-id="b6f15-123">Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="b6f15-123">Name of the offer.</span></span>

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

### <span data-ttu-id="b6f15-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b6f15-124">-Publisher</span></span>
<span data-ttu-id="b6f15-125">A közzétevő neve</span><span class="sxs-lookup"><span data-stu-id="b6f15-125">Name of the publisher.</span></span>

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

### <span data-ttu-id="b6f15-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="b6f15-126">-Sku</span></span>
<span data-ttu-id="b6f15-127">A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="b6f15-127">Name of the SKU.</span></span>

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

### <span data-ttu-id="b6f15-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6f15-128">-SubscriptionId</span></span>
<span data-ttu-id="b6f15-129">A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="b6f15-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b6f15-130">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b6f15-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b6f15-131">-Verzió</span><span class="sxs-lookup"><span data-stu-id="b6f15-131">-Version</span></span>
<span data-ttu-id="b6f15-132">Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="b6f15-132">The version of the resource.</span></span>

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

### <span data-ttu-id="b6f15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f15-133">CommonParameters</span></span>
<span data-ttu-id="b6f15-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b6f15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f15-135">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b6f15-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f15-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6f15-136">INPUTS</span></span>

### <span data-ttu-id="b6f15-137">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b6f15-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="b6f15-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6f15-138">OUTPUTS</span></span>

### <span data-ttu-id="b6f15-139">Microsoft. Azure. PowerShell. parancsmagok. ComputeAdmin. modellek. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="b6f15-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="b6f15-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b6f15-140">NOTES</span></span>

<span data-ttu-id="b6f15-141">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="b6f15-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6f15-142">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="b6f15-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b6f15-143">INPUTOBJECT <IComputeAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="b6f15-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6f15-144">`[DiskId <String>]`: A lemez GUID azonosítója identitásként.</span><span class="sxs-lookup"><span data-stu-id="b6f15-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="b6f15-145">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="b6f15-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6f15-146">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="b6f15-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b6f15-147">`[MigrationId <String>]`: Az áttelepítési feladat GUID-neve.</span><span class="sxs-lookup"><span data-stu-id="b6f15-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="b6f15-148">`[Offer <String>]`: Az ajánlat neve.</span><span class="sxs-lookup"><span data-stu-id="b6f15-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="b6f15-149">`[Publisher <String>]`: A közzétevő neve.</span><span class="sxs-lookup"><span data-stu-id="b6f15-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="b6f15-150">`[QuotaName <String>]`: A kvóta neve.</span><span class="sxs-lookup"><span data-stu-id="b6f15-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b6f15-151">`[Sku <String>]`: A SKU neve.</span><span class="sxs-lookup"><span data-stu-id="b6f15-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="b6f15-152">`[SubscriptionId <String>]`: A Microsoft Azure-előfizetést egyedileg azonosító hitelesítő adatok.</span><span class="sxs-lookup"><span data-stu-id="b6f15-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b6f15-153">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="b6f15-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b6f15-154">`[Type <String>]`: A kiterjesztés típusa.</span><span class="sxs-lookup"><span data-stu-id="b6f15-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="b6f15-155">`[Version <String>]`: Az erőforrás verziója.</span><span class="sxs-lookup"><span data-stu-id="b6f15-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="b6f15-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6f15-156">RELATED LINKS</span></span>

