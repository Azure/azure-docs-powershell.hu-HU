---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364487"
---
# <span data-ttu-id="a95e0-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="a95e0-101">Update-AzImportExport</span></span>

## <span data-ttu-id="a95e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a95e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a95e0-103">Frissíti egy feladat adott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a95e0-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="a95e0-104">Ezt a műveletet felhívva értesítheti az Importálás/exportálás szolgáltatást, hogy az importálási vagy exportálási feladatot tartalmazó merevlemezek a Microsoft adatközpontba került.</span><span class="sxs-lookup"><span data-stu-id="a95e0-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="a95e0-105">Egy meglévő feladat megszakítása is használható.</span><span class="sxs-lookup"><span data-stu-id="a95e0-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="a95e0-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a95e0-106">SYNTAX</span></span>

### <span data-ttu-id="a95e0-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a95e0-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a95e0-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a95e0-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a95e0-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a95e0-109">DESCRIPTION</span></span>
<span data-ttu-id="a95e0-110">Frissíti egy feladat adott tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="a95e0-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="a95e0-111">Ezt a műveletet felhívva értesítheti az Importálás/exportálás szolgáltatást, hogy az importálási vagy exportálási feladatot tartalmazó merevlemezek a Microsoft adatközpontba került.</span><span class="sxs-lookup"><span data-stu-id="a95e0-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="a95e0-112">Egy meglévő feladat megszakítása is használható.</span><span class="sxs-lookup"><span data-stu-id="a95e0-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="a95e0-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a95e0-113">EXAMPLES</span></span>

### <span data-ttu-id="a95e0-114">1. példa: Az ImportExport feladat frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="a95e0-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a95e0-115">Ez a parancsmag frissíti az ImportExport feladatot erőforráscsoport és kiszolgálónév szerint.</span><span class="sxs-lookup"><span data-stu-id="a95e0-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="a95e0-116">2. példa: Az ImportExport feladat frissítése identitás szerint.</span><span class="sxs-lookup"><span data-stu-id="a95e0-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="a95e0-117">Ez a parancsmag identitás szerint frissíti az ImportExport feladatot.</span><span class="sxs-lookup"><span data-stu-id="a95e0-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="a95e0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a95e0-118">PARAMETERS</span></span>

### <span data-ttu-id="a95e0-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="a95e0-119">-AcceptLanguage</span></span>
<span data-ttu-id="a95e0-120">A válasz elsődleges nyelvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a95e0-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="a95e0-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="a95e0-121">-BackupDriveManifest</span></span>
<span data-ttu-id="a95e0-122">Azt jelzi, hogy a meghajtókon lévő jegyzékfájlokat a blobok blokkolása miatt kell-e másolni.</span><span class="sxs-lookup"><span data-stu-id="a95e0-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="a95e0-123">-CancelRequested</span></span>
<span data-ttu-id="a95e0-124">Ha meg van adva, az értéknek igaznak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="a95e0-124">If specified, the value must be true.</span></span>
<span data-ttu-id="a95e0-125">A szolgáltatás megkísérli megszakítani a feladatot.</span><span class="sxs-lookup"><span data-stu-id="a95e0-125">The service will attempt to cancel the job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95e0-126">-DefaultProfile</span></span>
<span data-ttu-id="a95e0-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a95e0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95e0-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="a95e0-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="a95e0-129">Az importálási vagy exportálási meghajtók szállítására használt szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="a95e0-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="a95e0-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="a95e0-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="a95e0-131">A csomagban található meghajtók száma.</span><span class="sxs-lookup"><span data-stu-id="a95e0-131">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="a95e0-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="a95e0-133">A csomag szállításának dátuma.</span><span class="sxs-lookup"><span data-stu-id="a95e0-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="a95e0-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="a95e0-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="a95e0-135">A csomag nyomon követési száma.</span><span class="sxs-lookup"><span data-stu-id="a95e0-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="a95e0-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="a95e0-136">-DriveList</span></span>
<span data-ttu-id="a95e0-137">A feladatot magában foglaló meghajtók listája.</span><span class="sxs-lookup"><span data-stu-id="a95e0-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="a95e0-138">Ennek létrehozásáról a DRIVELIST tulajdonságokat és a kivonattáblát a MEGJEGYZÉSEK szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="a95e0-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a95e0-139">-InputObject</span></span>
<span data-ttu-id="a95e0-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="a95e0-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="a95e0-141">-LogLevel</span></span>
<span data-ttu-id="a95e0-142">Azt jelzi, hogy engedélyezve van-e a hibanaplózás vagy a részletes naplózás.</span><span class="sxs-lookup"><span data-stu-id="a95e0-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="a95e0-143">-Name</span><span class="sxs-lookup"><span data-stu-id="a95e0-143">-Name</span></span>
<span data-ttu-id="a95e0-144">Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="a95e0-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95e0-145">-ResourceGroupName</span></span>
<span data-ttu-id="a95e0-146">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="a95e0-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="a95e0-147">-ReturnAddressCity</span></span>
<span data-ttu-id="a95e0-148">A meghajtók visszaadásakor használt város neve.</span><span class="sxs-lookup"><span data-stu-id="a95e0-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="a95e0-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="a95e0-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="a95e0-150">A meghajtók visszaútjakor használt ország vagy régió.</span><span class="sxs-lookup"><span data-stu-id="a95e0-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="a95e0-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="a95e0-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="a95e0-152">A visszaküldött meghajtók címzettjének e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="a95e0-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="a95e0-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="a95e0-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="a95e0-154">A visszaadott meghajtók címzettjének telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="a95e0-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="a95e0-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="a95e0-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="a95e0-156">A meghajtók visszaadásakor használt irányítószám.</span><span class="sxs-lookup"><span data-stu-id="a95e0-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="a95e0-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="a95e0-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="a95e0-158">Annak a címzettnek a neve, aki a merevlemezeket visszaküldötte.</span><span class="sxs-lookup"><span data-stu-id="a95e0-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="a95e0-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="a95e0-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="a95e0-160">A meghajtók visszaadásakor használt állam vagy tartomány.</span><span class="sxs-lookup"><span data-stu-id="a95e0-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="a95e0-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="a95e0-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="a95e0-162">A meghajtók visszaadásakor használt utcacím első sora.</span><span class="sxs-lookup"><span data-stu-id="a95e0-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="a95e0-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="a95e0-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="a95e0-164">A meghajtók visszaútjakor használt utcacím második sora.</span><span class="sxs-lookup"><span data-stu-id="a95e0-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="a95e0-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="a95e0-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="a95e0-166">Az ügyfél ügyfél-száma a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="a95e0-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="a95e0-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="a95e0-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="a95e0-168">A szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="a95e0-168">The carrier's name.</span></span>

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

### <span data-ttu-id="a95e0-169">-State</span><span class="sxs-lookup"><span data-stu-id="a95e0-169">-State</span></span>
<span data-ttu-id="a95e0-170">Ha meg van adva, az értéknek szállításnak kell lennie, amely közli az Importálás/exportálás szolgáltatással, hogy a feladat csomagját kiszállították.</span><span class="sxs-lookup"><span data-stu-id="a95e0-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="a95e0-171">A ReturnAddress és a DeliveryPackage tulajdonságot vagy ebben a kérelemben, vagy egy korábbi kérésben be kell állítani, ellenkező esetben a kérés sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="a95e0-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="a95e0-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a95e0-172">-SubscriptionId</span></span>
<span data-ttu-id="a95e0-173">Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="a95e0-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="a95e0-174">-Tag</span></span>
<span data-ttu-id="a95e0-175">A feladathoz hozzárendelt címkéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="a95e0-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a95e0-176">-Confirm</span></span>
<span data-ttu-id="a95e0-177">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a95e0-177">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95e0-178">-WhatIf</span></span>
<span data-ttu-id="a95e0-179">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a95e0-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a95e0-180">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a95e0-180">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95e0-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95e0-181">CommonParameters</span></span>
<span data-ttu-id="a95e0-182">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95e0-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95e0-183">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a95e0-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95e0-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a95e0-184">INPUTS</span></span>

### <span data-ttu-id="a95e0-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="a95e0-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="a95e0-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a95e0-186">OUTPUTS</span></span>

### <span data-ttu-id="a95e0-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="a95e0-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="a95e0-188">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a95e0-188">NOTES</span></span>

<span data-ttu-id="a95e0-189">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a95e0-189">ALIASES</span></span>

<span data-ttu-id="a95e0-190">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="a95e0-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a95e0-191">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="a95e0-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a95e0-192">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a95e0-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a95e0-193">DRIVELIST <IDriveStatus[]>: A feladatot magában foglaló meghajtók listája.</span><span class="sxs-lookup"><span data-stu-id="a95e0-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="a95e0-194">`[BitLockerKey <String>]`: A meghajtó titkosításához használt BitLocker kulcs.</span><span class="sxs-lookup"><span data-stu-id="a95e0-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="a95e0-195">`[BytesSucceeded <Int64?>]`: A meghajtóhoz bájtok átvitele sikerült.</span><span class="sxs-lookup"><span data-stu-id="a95e0-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="a95e0-196">`[CopyStatus <String>]`: Az adatátviteli folyamat részletes állapota.</span><span class="sxs-lookup"><span data-stu-id="a95e0-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="a95e0-197">Ez a mező mindaddig nem ad vissza a válaszban, amíg a meghajtó átvitt állapotba nem áll.</span><span class="sxs-lookup"><span data-stu-id="a95e0-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="a95e0-198">`[DriveHeaderHash <String>]`: A meghajtófejléc kivonatának értéke.</span><span class="sxs-lookup"><span data-stu-id="a95e0-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="a95e0-199">`[DriveId <String>]`: A meghajtó hardveres sorozatszáma szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="a95e0-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="a95e0-200">`[ErrorLogUri <String>]`: Egy URI, amely az adatátviteli művelet hibanaplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="a95e0-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="a95e0-201">`[ManifestFile <String>]`: A jegyzékfájl relatív elérési útja a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="a95e0-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="a95e0-202">`[ManifestHash <String>]`: A meghajtón található jegyzékfájl Base16 kódolású MD5-kivonata.</span><span class="sxs-lookup"><span data-stu-id="a95e0-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="a95e0-203">`[ManifestUri <String>]`: Egy URI, amely a meghajtó jegyzékfájlját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="a95e0-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="a95e0-204">`[PercentComplete <Int32?>]`: A meghajtóra vonatkozó százalékos érték.</span><span class="sxs-lookup"><span data-stu-id="a95e0-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="a95e0-205">`[State <DriveState?>]`: A meghajtó aktuális állapota.</span><span class="sxs-lookup"><span data-stu-id="a95e0-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="a95e0-206">`[VerboseLogUri <String>]`: Egy URI, amely az adatátviteli művelet részletes naplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="a95e0-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="a95e0-207">INPUTOBJECT: <IImportExportIdentity> Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="a95e0-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a95e0-208">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="a95e0-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a95e0-209">`[JobName <String>]`: Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="a95e0-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="a95e0-210">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="a95e0-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="a95e0-211">Ilyen például az Egyesült Államok nyugati és nyugati régiója.</span><span class="sxs-lookup"><span data-stu-id="a95e0-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="a95e0-212">`[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="a95e0-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="a95e0-213">`[SubscriptionId <String>]`: Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="a95e0-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="a95e0-214">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a95e0-214">RELATED LINKS</span></span>

