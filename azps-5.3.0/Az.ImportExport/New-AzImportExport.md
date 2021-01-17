---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480274"
---
# <span data-ttu-id="5d55a-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="5d55a-101">New-AzImportExport</span></span>

## <span data-ttu-id="5d55a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d55a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d55a-103">Új feladatot hoz létre, vagy frissíti a megadott előfizetésben meglévő feladatot.</span><span class="sxs-lookup"><span data-stu-id="5d55a-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="5d55a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5d55a-104">SYNTAX</span></span>

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

## <span data-ttu-id="5d55a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5d55a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d55a-106">Új feladatot hoz létre, vagy frissíti a megadott előfizetésben meglévő feladatot.</span><span class="sxs-lookup"><span data-stu-id="5d55a-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="5d55a-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5d55a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d55a-108">1. példa: Új ImportExport feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="5d55a-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="5d55a-109">Ezek a parancsmagok új ImportExport feladatot hoznak létre.</span><span class="sxs-lookup"><span data-stu-id="5d55a-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="5d55a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d55a-110">PARAMETERS</span></span>

### <span data-ttu-id="5d55a-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="5d55a-111">-AcceptLanguage</span></span>
<span data-ttu-id="5d55a-112">A válasz elsődleges nyelvét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5d55a-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="5d55a-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="5d55a-113">-BackupDriveManifest</span></span>
<span data-ttu-id="5d55a-114">Az alapértelmezett érték hamis.</span><span class="sxs-lookup"><span data-stu-id="5d55a-114">Default value is false.</span></span>
<span data-ttu-id="5d55a-115">Azt jelzi, hogy a meghajtókon lévő jegyzékfájlokat a blobok blokkolása miatt kell-e másolni.</span><span class="sxs-lookup"><span data-stu-id="5d55a-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="5d55a-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="5d55a-116">-BlobListBlobPath</span></span>
<span data-ttu-id="5d55a-117">Blob-path karakterláncok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="5d55a-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="5d55a-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="5d55a-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="5d55a-119">Blob-előtag karakterláncok gyűjteménye.</span><span class="sxs-lookup"><span data-stu-id="5d55a-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="5d55a-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="5d55a-120">-CancelRequested</span></span>
<span data-ttu-id="5d55a-121">Azt jelzi, hogy elküldték-e a feladat lemondását igénylésként.</span><span class="sxs-lookup"><span data-stu-id="5d55a-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="5d55a-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="5d55a-122">-ClientTenantId</span></span>
<span data-ttu-id="5d55a-123">A kérelmet bekért ügyfél bérlőazonosítója.</span><span class="sxs-lookup"><span data-stu-id="5d55a-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="5d55a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d55a-124">-DefaultProfile</span></span>
<span data-ttu-id="5d55a-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d55a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d55a-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="5d55a-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="5d55a-127">Az importálási vagy exportálási meghajtók szállítására használt szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="5d55a-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="5d55a-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="5d55a-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="5d55a-129">A csomagban található meghajtók száma.</span><span class="sxs-lookup"><span data-stu-id="5d55a-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="5d55a-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="5d55a-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="5d55a-131">A csomag szállításának dátuma.</span><span class="sxs-lookup"><span data-stu-id="5d55a-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="5d55a-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="5d55a-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="5d55a-133">A csomag nyomon követési száma.</span><span class="sxs-lookup"><span data-stu-id="5d55a-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="5d55a-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="5d55a-134">-DiagnosticsPath</span></span>
<span data-ttu-id="5d55a-135">Az a virtuális blobtár, amelybe a meghajtó jegyzékfájl-fájljainak másolási naplói és biztonsági másolatai (ha engedélyezve vannak) tárolódnak.</span><span class="sxs-lookup"><span data-stu-id="5d55a-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="5d55a-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="5d55a-136">-DriveList</span></span>
<span data-ttu-id="5d55a-137">A feladatot magában foglaló legfeljebb tíz meghajtó listája.</span><span class="sxs-lookup"><span data-stu-id="5d55a-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="5d55a-138">A meghajtólista egy importálási feladat kötelező eleme; az exportálási feladatokhoz nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="5d55a-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="5d55a-139">Ennek létrehozásáról a DRIVELIST tulajdonságokat és a kivonattáblát a MEGJEGYZÉSEK szakaszban láthatja.</span><span class="sxs-lookup"><span data-stu-id="5d55a-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d55a-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="5d55a-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="5d55a-141">A blobblokk relatív URI-val való viszonya, amely a fenti blob elérési utak vagy blob elérési utak listáját tartalmazza, a tároló nevével kezdve.</span><span class="sxs-lookup"><span data-stu-id="5d55a-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="5d55a-142">Ha a blob gyökértárolóban van, az URI-nak egy másik $root.</span><span class="sxs-lookup"><span data-stu-id="5d55a-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="5d55a-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="5d55a-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="5d55a-144">Olyan blob elérési útja, amely a nem exportált blobneveket tartalmazó blokk blobra mutat, mert nincs elegendő meghajtótér.</span><span class="sxs-lookup"><span data-stu-id="5d55a-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="5d55a-145">Ha az összes blob exportálása sikerült, akkor ez az elem nem szerepel a válaszban.</span><span class="sxs-lookup"><span data-stu-id="5d55a-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="5d55a-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="5d55a-146">-JobType</span></span>
<span data-ttu-id="5d55a-147">A feladat típusa</span><span class="sxs-lookup"><span data-stu-id="5d55a-147">The type of job</span></span>

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

### <span data-ttu-id="5d55a-148">-Location</span><span class="sxs-lookup"><span data-stu-id="5d55a-148">-Location</span></span>
<span data-ttu-id="5d55a-149">Megadja a támogatott Azure-helyet, ahol létre kell hozatni a feladatot</span><span class="sxs-lookup"><span data-stu-id="5d55a-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="5d55a-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="5d55a-150">-LogLevel</span></span>
<span data-ttu-id="5d55a-151">Az alapértelmezett érték a Hiba.</span><span class="sxs-lookup"><span data-stu-id="5d55a-151">Default value is Error.</span></span>
<span data-ttu-id="5d55a-152">Azt jelzi, hogy engedélyezve van-e a hiba- vagy részletes naplózás.</span><span class="sxs-lookup"><span data-stu-id="5d55a-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="5d55a-153">-Name</span><span class="sxs-lookup"><span data-stu-id="5d55a-153">-Name</span></span>
<span data-ttu-id="5d55a-154">Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="5d55a-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="5d55a-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="5d55a-155">-PercentComplete</span></span>
<span data-ttu-id="5d55a-156">A feladathoz adott teljes százalékos érték.</span><span class="sxs-lookup"><span data-stu-id="5d55a-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="5d55a-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="5d55a-157">-ProvisioningState</span></span>
<span data-ttu-id="5d55a-158">A feladat kiépítési állapotát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="5d55a-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="5d55a-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d55a-159">-ResourceGroupName</span></span>
<span data-ttu-id="5d55a-160">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="5d55a-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="5d55a-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="5d55a-161">-ReturnAddressCity</span></span>
<span data-ttu-id="5d55a-162">A meghajtók visszaadásakor használt város neve.</span><span class="sxs-lookup"><span data-stu-id="5d55a-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="5d55a-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="5d55a-164">A meghajtók visszaútjakor használt ország vagy régió.</span><span class="sxs-lookup"><span data-stu-id="5d55a-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="5d55a-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="5d55a-166">A visszaküldött meghajtók címzettjének e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="5d55a-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="5d55a-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="5d55a-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="5d55a-168">A visszaadott meghajtók címzettjének telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="5d55a-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="5d55a-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="5d55a-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="5d55a-170">A meghajtók visszaadásakor használt irányítószám.</span><span class="sxs-lookup"><span data-stu-id="5d55a-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="5d55a-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="5d55a-172">Annak a címzettnek a neve, aki a merevlemezeket visszaküldötte.</span><span class="sxs-lookup"><span data-stu-id="5d55a-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="5d55a-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="5d55a-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="5d55a-174">A meghajtók visszaadásakor használt állam vagy tartomány.</span><span class="sxs-lookup"><span data-stu-id="5d55a-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="5d55a-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="5d55a-176">A meghajtók visszaadásakor használt utcacím első sora.</span><span class="sxs-lookup"><span data-stu-id="5d55a-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="5d55a-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="5d55a-178">A meghajtók visszaútjakor használt utcacím második sora.</span><span class="sxs-lookup"><span data-stu-id="5d55a-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="5d55a-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="5d55a-180">Az importálási vagy exportálási meghajtók szállítására használt szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="5d55a-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="5d55a-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="5d55a-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="5d55a-182">A csomagban található meghajtók száma.</span><span class="sxs-lookup"><span data-stu-id="5d55a-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="5d55a-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="5d55a-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="5d55a-184">A csomag szállításának dátuma.</span><span class="sxs-lookup"><span data-stu-id="5d55a-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="5d55a-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="5d55a-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="5d55a-186">A csomag nyomon követési száma.</span><span class="sxs-lookup"><span data-stu-id="5d55a-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="5d55a-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="5d55a-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="5d55a-188">Az ügyfél ügyfél-száma a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="5d55a-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="5d55a-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="5d55a-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="5d55a-190">A szolgáltató neve.</span><span class="sxs-lookup"><span data-stu-id="5d55a-190">The carrier's name.</span></span>

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

### <span data-ttu-id="5d55a-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="5d55a-191">-ShippingInformationCity</span></span>
<span data-ttu-id="5d55a-192">A meghajtók visszaadásakor használt város neve.</span><span class="sxs-lookup"><span data-stu-id="5d55a-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="5d55a-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="5d55a-194">A meghajtók visszaútjakor használt ország vagy régió.</span><span class="sxs-lookup"><span data-stu-id="5d55a-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="5d55a-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="5d55a-196">A visszaadott meghajtók címzettjének telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="5d55a-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="5d55a-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="5d55a-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="5d55a-198">A meghajtók visszaadásakor használt irányítószám.</span><span class="sxs-lookup"><span data-stu-id="5d55a-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="5d55a-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="5d55a-200">Annak a címzettnek a neve, aki a merevlemezeket visszaküldötte.</span><span class="sxs-lookup"><span data-stu-id="5d55a-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="5d55a-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="5d55a-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="5d55a-202">A meghajtók visszaadásakor használt állam vagy tartomány.</span><span class="sxs-lookup"><span data-stu-id="5d55a-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="5d55a-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="5d55a-204">A meghajtók visszaadásakor használt utcacím első sora.</span><span class="sxs-lookup"><span data-stu-id="5d55a-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="5d55a-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="5d55a-206">A meghajtók visszaútjakor használt utcacím második sora.</span><span class="sxs-lookup"><span data-stu-id="5d55a-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="5d55a-207">-State</span><span class="sxs-lookup"><span data-stu-id="5d55a-207">-State</span></span>
<span data-ttu-id="5d55a-208">A feladat aktuális állapota.</span><span class="sxs-lookup"><span data-stu-id="5d55a-208">Current state of the job.</span></span>

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

### <span data-ttu-id="5d55a-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5d55a-209">-StorageAccountId</span></span>
<span data-ttu-id="5d55a-210">Annak a tárfióknak az erőforrás-azonosítója, amelybe importálni vagy exportálni fogja az adatokat.</span><span class="sxs-lookup"><span data-stu-id="5d55a-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="5d55a-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d55a-211">-SubscriptionId</span></span>
<span data-ttu-id="5d55a-212">Az Azure-felhasználó előfizetésazonosítója.</span><span class="sxs-lookup"><span data-stu-id="5d55a-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="5d55a-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d55a-213">-Tag</span></span>
<span data-ttu-id="5d55a-214">A feladathoz hozzárendelt címkéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="5d55a-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="5d55a-215">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d55a-215">-Confirm</span></span>
<span data-ttu-id="5d55a-216">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5d55a-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d55a-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d55a-217">-WhatIf</span></span>
<span data-ttu-id="5d55a-218">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5d55a-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d55a-219">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5d55a-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d55a-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d55a-220">CommonParameters</span></span>
<span data-ttu-id="5d55a-221">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d55a-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d55a-222">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d55a-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d55a-223">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d55a-223">INPUTS</span></span>

## <span data-ttu-id="5d55a-224">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d55a-224">OUTPUTS</span></span>

### <span data-ttu-id="5d55a-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="5d55a-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="5d55a-226">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5d55a-226">NOTES</span></span>

<span data-ttu-id="5d55a-227">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5d55a-227">ALIASES</span></span>

<span data-ttu-id="5d55a-228">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="5d55a-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d55a-229">Az alább ismertetett paraméterek létrehozásához hozzon létre egy olyan kivonattáblát, amely tartalmazza a megfelelő tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="5d55a-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d55a-230">A kivonattáblákról további információt a Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d55a-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d55a-231">DRIVELIST <IDriveStatus[]>: A feladatot magában foglaló legfeljebb tíz meghajtó listája.</span><span class="sxs-lookup"><span data-stu-id="5d55a-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="5d55a-232">A meghajtólista egy importálási feladat kötelező eleme; az exportálási feladatokhoz nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="5d55a-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="5d55a-233">`[BitLockerKey <String>]`: A meghajtó titkosításához használt BitLocker kulcs.</span><span class="sxs-lookup"><span data-stu-id="5d55a-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="5d55a-234">`[BytesSucceeded <Int64?>]`: A meghajtóhoz bájtok átvitele sikerült.</span><span class="sxs-lookup"><span data-stu-id="5d55a-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="5d55a-235">`[CopyStatus <String>]`: Az adatátviteli folyamat részletes állapota.</span><span class="sxs-lookup"><span data-stu-id="5d55a-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="5d55a-236">Ez a mező mindaddig nem ad vissza a válaszban, amíg a meghajtó átvitt állapotba nem áll.</span><span class="sxs-lookup"><span data-stu-id="5d55a-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="5d55a-237">`[DriveHeaderHash <String>]`: A meghajtófejléc kivonatának értéke.</span><span class="sxs-lookup"><span data-stu-id="5d55a-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="5d55a-238">`[DriveId <String>]`: A meghajtó hardveres sorozatszáma szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="5d55a-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="5d55a-239">`[ErrorLogUri <String>]`: Egy URI, amely az adatátviteli művelet hibanaplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="5d55a-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="5d55a-240">`[ManifestFile <String>]`: A jegyzékfájl relatív elérési útja a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="5d55a-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="5d55a-241">`[ManifestHash <String>]`: A meghajtón található jegyzékfájl Base16 kódolású MD5-kivonata.</span><span class="sxs-lookup"><span data-stu-id="5d55a-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="5d55a-242">`[ManifestUri <String>]`: Egy URI, amely a meghajtó jegyzékfájlját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="5d55a-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="5d55a-243">`[PercentComplete <Int32?>]`: A meghajtóra vonatkozó százalékos érték.</span><span class="sxs-lookup"><span data-stu-id="5d55a-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="5d55a-244">`[State <DriveState?>]`: A meghajtó aktuális állapota.</span><span class="sxs-lookup"><span data-stu-id="5d55a-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="5d55a-245">`[VerboseLogUri <String>]`: Egy URI, amely az adatátviteli művelet részletes naplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="5d55a-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="5d55a-246">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d55a-246">RELATED LINKS</span></span>

