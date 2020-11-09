---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296240"
---
# <span data-ttu-id="87a00-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="87a00-101">New-AzImportExport</span></span>

## <span data-ttu-id="87a00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87a00-102">SYNOPSIS</span></span>
<span data-ttu-id="87a00-103">Új feladatot hoz létre, vagy egy meglévő feladatot frissít a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="87a00-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="87a00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87a00-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="87a00-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87a00-105">DESCRIPTION</span></span>
<span data-ttu-id="87a00-106">Új feladatot hoz létre, vagy egy meglévő feladatot frissít a megadott előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="87a00-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="87a00-107">Példák</span><span class="sxs-lookup"><span data-stu-id="87a00-107">EXAMPLES</span></span>

### <span data-ttu-id="87a00-108">Példa 1: új ImportExport-feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="87a00-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="87a00-109">Ezekkel a parancsmagokkal új ImportExport-feladatot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="87a00-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="87a00-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87a00-110">PARAMETERS</span></span>

### <span data-ttu-id="87a00-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="87a00-111">-AcceptLanguage</span></span>
<span data-ttu-id="87a00-112">A válasz kívánt nyelvét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87a00-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="87a00-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="87a00-113">-BackupDriveManifest</span></span>
<span data-ttu-id="87a00-114">Az alapértelmezett érték a hamis.</span><span class="sxs-lookup"><span data-stu-id="87a00-114">Default value is false.</span></span>
<span data-ttu-id="87a00-115">Azt jelzi, hogy a meghajtókban lévő MANIFEST-fájlokat másolni kell-e a blobokra.</span><span class="sxs-lookup"><span data-stu-id="87a00-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="87a00-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="87a00-116">-BlobListBlobPath</span></span>
<span data-ttu-id="87a00-117">BLOB-Path karakterláncok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="87a00-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a00-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="87a00-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="87a00-119">BLOB-előtagot tartalmazó karakterláncok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="87a00-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a00-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="87a00-120">-CancelRequested</span></span>
<span data-ttu-id="87a00-121">Azt jelzi, hogy elküldtek-e kérést a feladat visszavonásához.</span><span class="sxs-lookup"><span data-stu-id="87a00-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="87a00-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="87a00-122">-ClientTenantId</span></span>
<span data-ttu-id="87a00-123">A kérelmet készítő ügyfél bérlői azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87a00-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="87a00-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a00-124">-DefaultProfile</span></span>
<span data-ttu-id="87a00-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87a00-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a00-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="87a00-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="87a00-127">Annak a szolgáltatónak a neve, amely az importálási vagy exportálási meghajtók szállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="87a00-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="87a00-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="87a00-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="87a00-129">A csomagban található meghajtók száma.</span><span class="sxs-lookup"><span data-stu-id="87a00-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="87a00-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="87a00-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="87a00-131">A csomag leszállításának dátuma.</span><span class="sxs-lookup"><span data-stu-id="87a00-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="87a00-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="87a00-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="87a00-133">A csomag nyilvántartási száma.</span><span class="sxs-lookup"><span data-stu-id="87a00-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="87a00-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="87a00-134">-DiagnosticsPath</span></span>
<span data-ttu-id="87a00-135">A virtuális blob-könyvtár, amelyre a Drive manifest-fájlok másolása és biztonsági másolatai (ha engedélyezve vannak) tárolása megtörténik.</span><span class="sxs-lookup"><span data-stu-id="87a00-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="87a00-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="87a00-136">-DriveList</span></span>
<span data-ttu-id="87a00-137">A feladatot tartalmazó legfeljebb tíz meghajtó listája.</span><span class="sxs-lookup"><span data-stu-id="87a00-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="87a00-138">A lemezmeghajtók listája az importálási feladat kötelező eleme; nincs megadva az exportálási feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="87a00-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="87a00-139">A kivitelezéshez tekintse meg a DRIVELIST tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="87a00-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="87a00-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="87a00-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="87a00-141">A fentiekben ismertetett blob-görbék vagy blob-elérési utak előtagjainak listáját tartalmazó blokk blob a relatív URI-azonosítóval, a tároló nevétől kezdve.</span><span class="sxs-lookup"><span data-stu-id="87a00-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="87a00-142">Ha a blob a legfelső szintű tárolóban van, az URI-nek $root kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="87a00-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="87a00-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="87a00-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="87a00-144">Egy olyan blob-elérési út, amely a nem elegendő szabad tárterület miatt nem exportált blob-nevek listáját a blokk blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="87a00-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="87a00-145">Ha minden blob exportálása sikerült, akkor ez az elem nem szerepel a válaszban.</span><span class="sxs-lookup"><span data-stu-id="87a00-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="87a00-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="87a00-146">-JobType</span></span>
<span data-ttu-id="87a00-147">A feladat típusa</span><span class="sxs-lookup"><span data-stu-id="87a00-147">The type of job</span></span>

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

### <span data-ttu-id="87a00-148">-Hely</span><span class="sxs-lookup"><span data-stu-id="87a00-148">-Location</span></span>
<span data-ttu-id="87a00-149">Annak a támogatott Azure-helynek a meghatározása, ahol a feladatot létre kell tenni</span><span class="sxs-lookup"><span data-stu-id="87a00-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="87a00-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="87a00-150">-LogLevel</span></span>
<span data-ttu-id="87a00-151">Az alapértelmezett érték a hiba.</span><span class="sxs-lookup"><span data-stu-id="87a00-151">Default value is Error.</span></span>
<span data-ttu-id="87a00-152">Azt jelzi, hogy engedélyezve van-e a hibák naplózása vagy a részletes naplózás.</span><span class="sxs-lookup"><span data-stu-id="87a00-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="87a00-153">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87a00-153">-Name</span></span>
<span data-ttu-id="87a00-154">Az Importálás/exportálás feladat neve.</span><span class="sxs-lookup"><span data-stu-id="87a00-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a00-155">-KészültségiSzint paraméter értéke</span><span class="sxs-lookup"><span data-stu-id="87a00-155">-PercentComplete</span></span>
<span data-ttu-id="87a00-156">A projekthez befejezett teljes készültségi érték</span><span class="sxs-lookup"><span data-stu-id="87a00-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="87a00-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="87a00-157">-ProvisioningState</span></span>
<span data-ttu-id="87a00-158">A feladat kiépítési állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="87a00-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="87a00-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a00-159">-ResourceGroupName</span></span>
<span data-ttu-id="87a00-160">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="87a00-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a00-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="87a00-161">-ReturnAddressCity</span></span>
<span data-ttu-id="87a00-162">A lemezmeghajtók visszatéréséhez használandó település neve.</span><span class="sxs-lookup"><span data-stu-id="87a00-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="87a00-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="87a00-164">A meghajtók visszaadása során használandó ország vagy régió.</span><span class="sxs-lookup"><span data-stu-id="87a00-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="87a00-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="87a00-166">A visszaadott meghajtók címzettje e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="87a00-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="87a00-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="87a00-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="87a00-168">A visszaadott meghajtók címzettjeinek telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="87a00-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="87a00-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="87a00-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="87a00-170">A lemezmeghajtók visszatéréséhez használandó irányítószám.</span><span class="sxs-lookup"><span data-stu-id="87a00-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="87a00-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="87a00-172">Annak a címzettnek a neve, aki a visszatéréskor a merevlemezt fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="87a00-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="87a00-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="87a00-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="87a00-174">A meghajtók visszatéréséhez használandó állam vagy tartomány.</span><span class="sxs-lookup"><span data-stu-id="87a00-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="87a00-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="87a00-176">A lemezmeghajtók visszatéréséhez használandó utcanév első sora.</span><span class="sxs-lookup"><span data-stu-id="87a00-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="87a00-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="87a00-178">A lemezmeghajtók visszatéréséhez használandó utcanév második sora.</span><span class="sxs-lookup"><span data-stu-id="87a00-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="87a00-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="87a00-180">Annak a szolgáltatónak a neve, amely az importálási vagy exportálási meghajtók szállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="87a00-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="87a00-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="87a00-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="87a00-182">A csomagban található meghajtók száma.</span><span class="sxs-lookup"><span data-stu-id="87a00-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="87a00-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="87a00-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="87a00-184">A csomag leszállításának dátuma.</span><span class="sxs-lookup"><span data-stu-id="87a00-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="87a00-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="87a00-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="87a00-186">A csomag nyilvántartási száma.</span><span class="sxs-lookup"><span data-stu-id="87a00-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="87a00-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="87a00-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="87a00-188">Az ügyfél számlaszáma a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="87a00-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="87a00-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="87a00-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="87a00-190">A fuvarozó neve.</span><span class="sxs-lookup"><span data-stu-id="87a00-190">The carrier's name.</span></span>

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

### <span data-ttu-id="87a00-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="87a00-191">-ShippingInformationCity</span></span>
<span data-ttu-id="87a00-192">A lemezmeghajtók visszatéréséhez használandó település neve.</span><span class="sxs-lookup"><span data-stu-id="87a00-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="87a00-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="87a00-194">A meghajtók visszaadása során használandó ország vagy régió.</span><span class="sxs-lookup"><span data-stu-id="87a00-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="87a00-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="87a00-196">A visszaadott meghajtók címzettjeinek telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="87a00-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="87a00-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="87a00-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="87a00-198">A lemezmeghajtók visszatéréséhez használandó irányítószám.</span><span class="sxs-lookup"><span data-stu-id="87a00-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="87a00-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="87a00-200">Annak a címzettnek a neve, aki a visszatéréskor a merevlemezt fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="87a00-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="87a00-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="87a00-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="87a00-202">A meghajtók visszatéréséhez használandó állam vagy tartomány.</span><span class="sxs-lookup"><span data-stu-id="87a00-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="87a00-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="87a00-204">A lemezmeghajtók visszatéréséhez használandó utcanév első sora.</span><span class="sxs-lookup"><span data-stu-id="87a00-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="87a00-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="87a00-206">A lemezmeghajtók visszatéréséhez használandó utcanév második sora.</span><span class="sxs-lookup"><span data-stu-id="87a00-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="87a00-207">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="87a00-207">-State</span></span>
<span data-ttu-id="87a00-208">A feladat aktuális állapota.</span><span class="sxs-lookup"><span data-stu-id="87a00-208">Current state of the job.</span></span>

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

### <span data-ttu-id="87a00-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="87a00-209">-StorageAccountId</span></span>
<span data-ttu-id="87a00-210">Annak a tárolási fióknak az erőforrás-azonosítója, amelybe az adatot importálja vagy onnan exportálja a program.</span><span class="sxs-lookup"><span data-stu-id="87a00-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="87a00-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87a00-211">-SubscriptionId</span></span>
<span data-ttu-id="87a00-212">Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="87a00-212">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a00-213">-Címke</span><span class="sxs-lookup"><span data-stu-id="87a00-213">-Tag</span></span>
<span data-ttu-id="87a00-214">A feladathoz hozzárendelni kívánt címkéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="87a00-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87a00-215">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87a00-215">-Confirm</span></span>
<span data-ttu-id="87a00-216">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87a00-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a00-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a00-217">-WhatIf</span></span>
<span data-ttu-id="87a00-218">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87a00-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87a00-219">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87a00-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a00-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a00-220">CommonParameters</span></span>
<span data-ttu-id="87a00-221">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87a00-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a00-222">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="87a00-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a00-223">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87a00-223">INPUTS</span></span>

## <span data-ttu-id="87a00-224">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87a00-224">OUTPUTS</span></span>

### <span data-ttu-id="87a00-225">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. modellek. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="87a00-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="87a00-226">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87a00-226">NOTES</span></span>

<span data-ttu-id="87a00-227">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="87a00-227">ALIASES</span></span>

<span data-ttu-id="87a00-228">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="87a00-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87a00-229">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="87a00-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87a00-230">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="87a00-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87a00-231">DRIVELIST <IDriveStatus [] >: a feladatot tartalmazó legfeljebb tíz meghajtó listája.</span><span class="sxs-lookup"><span data-stu-id="87a00-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="87a00-232">A lemezmeghajtók listája az importálási feladat kötelező eleme; nincs megadva az exportálási feladatokhoz.</span><span class="sxs-lookup"><span data-stu-id="87a00-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="87a00-233">`[BitLockerKey <String>]`: A meghajtó titkosításához használt BitLocker-kulcs.</span><span class="sxs-lookup"><span data-stu-id="87a00-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="87a00-234">`[BytesSucceeded <Int64?>]`: Sikeresen átvitt bájtok a meghajtóra.</span><span class="sxs-lookup"><span data-stu-id="87a00-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="87a00-235">`[CopyStatus <String>]`: Az adatátviteli folyamat részletes állapota.</span><span class="sxs-lookup"><span data-stu-id="87a00-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="87a00-236">Ezt a mezőt addig nem adja vissza a válasz, amíg a meghajtó az átadó államban van.</span><span class="sxs-lookup"><span data-stu-id="87a00-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="87a00-237">`[DriveHeaderHash <String>]`: A meghajtó fejléc-ujjlenyomatának értéke.</span><span class="sxs-lookup"><span data-stu-id="87a00-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="87a00-238">`[DriveId <String>]`: A meghajtó hardveres sorozatszáma szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="87a00-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="87a00-239">`[ErrorLogUri <String>]`: Egy URI, amely az adatátviteli művelethez az adattovábbítási művelethez tartozó hibát tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="87a00-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="87a00-240">`[ManifestFile <String>]`: A manifest-fájl relatív elérési útja a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="87a00-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="87a00-241">`[ManifestHash <String>]`: A manifest-fájl Base16 kódolt MD5 hash-je a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="87a00-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="87a00-242">`[ManifestUri <String>]`: A Drive manifest-fájlt tartalmazó blobra mutató URI.</span><span class="sxs-lookup"><span data-stu-id="87a00-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="87a00-243">`[PercentComplete <Int32?>]`: Készültségi% a meghajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="87a00-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="87a00-244">`[State <DriveState?>]`: A meghajtó jelenlegi állapota.</span><span class="sxs-lookup"><span data-stu-id="87a00-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="87a00-245">`[VerboseLogUri <String>]`: Egy URI, amely az adatátviteli művelet részletes naplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="87a00-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="87a00-246">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87a00-246">RELATED LINKS</span></span>

