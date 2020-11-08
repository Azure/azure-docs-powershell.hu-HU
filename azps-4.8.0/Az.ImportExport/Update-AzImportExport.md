---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182213"
---
# <span data-ttu-id="1691a-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="1691a-101">Update-AzImportExport</span></span>

## <span data-ttu-id="1691a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1691a-102">SYNOPSIS</span></span>
<span data-ttu-id="1691a-103">A feladatok bizonyos tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="1691a-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="1691a-104">Ezt a műveletet felhívhatja az importálási/exportálási szolgáltatás értesítésére, hogy az importálási vagy exportálási feladatot tartalmazó merevlemezek a Microsoft-adatközpontba lettek szállítva.</span><span class="sxs-lookup"><span data-stu-id="1691a-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="1691a-105">A meglévő feladatok visszavonására is használható.</span><span class="sxs-lookup"><span data-stu-id="1691a-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="1691a-106">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1691a-106">SYNTAX</span></span>

### <span data-ttu-id="1691a-107">UpdateExpanded (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1691a-107">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="1691a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1691a-108">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="1691a-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="1691a-109">DESCRIPTION</span></span>
<span data-ttu-id="1691a-110">A feladatok bizonyos tulajdonságait frissíti.</span><span class="sxs-lookup"><span data-stu-id="1691a-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="1691a-111">Ezt a műveletet felhívhatja az importálási/exportálási szolgáltatás értesítésére, hogy az importálási vagy exportálási feladatot tartalmazó merevlemezek a Microsoft-adatközpontba lettek szállítva.</span><span class="sxs-lookup"><span data-stu-id="1691a-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="1691a-112">A meglévő feladatok visszavonására is használható.</span><span class="sxs-lookup"><span data-stu-id="1691a-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="1691a-113">Példák</span><span class="sxs-lookup"><span data-stu-id="1691a-113">EXAMPLES</span></span>

### <span data-ttu-id="1691a-114">Példa 1: ImportExport feladat frissítése erőforráscsoport és kiszolgálónév szerint</span><span class="sxs-lookup"><span data-stu-id="1691a-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="1691a-115">Ez a parancsmag a ImportExport-feladatot az erőforráscsoport és a kiszolgáló neve szerint frissíti.</span><span class="sxs-lookup"><span data-stu-id="1691a-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="1691a-116">2. példa: ImportExport-feladat frissítése identitással.</span><span class="sxs-lookup"><span data-stu-id="1691a-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="1691a-117">Ez a parancsmag a ImportExport-feladatot identitással frissíti.</span><span class="sxs-lookup"><span data-stu-id="1691a-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="1691a-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1691a-118">PARAMETERS</span></span>

### <span data-ttu-id="1691a-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="1691a-119">-AcceptLanguage</span></span>
<span data-ttu-id="1691a-120">A válasz kívánt nyelvét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1691a-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="1691a-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="1691a-121">-BackupDriveManifest</span></span>
<span data-ttu-id="1691a-122">Azt jelzi, hogy a meghajtókban lévő MANIFEST-fájlokat másolni kell-e a blobokra.</span><span class="sxs-lookup"><span data-stu-id="1691a-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="1691a-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="1691a-123">-CancelRequested</span></span>
<span data-ttu-id="1691a-124">Ha meg van adva, az értéknek igaznak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="1691a-124">If specified, the value must be true.</span></span>
<span data-ttu-id="1691a-125">A szolgáltatás megkísérli lemondani a feladatot.</span><span class="sxs-lookup"><span data-stu-id="1691a-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="1691a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1691a-126">-DefaultProfile</span></span>
<span data-ttu-id="1691a-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1691a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1691a-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="1691a-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="1691a-129">Annak a szolgáltatónak a neve, amely az importálási vagy exportálási meghajtók szállítására szolgál.</span><span class="sxs-lookup"><span data-stu-id="1691a-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="1691a-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="1691a-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="1691a-131">A csomagban található meghajtók száma.</span><span class="sxs-lookup"><span data-stu-id="1691a-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="1691a-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="1691a-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="1691a-133">A csomag leszállításának dátuma.</span><span class="sxs-lookup"><span data-stu-id="1691a-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="1691a-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="1691a-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="1691a-135">A csomag nyilvántartási száma.</span><span class="sxs-lookup"><span data-stu-id="1691a-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="1691a-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="1691a-136">-DriveList</span></span>
<span data-ttu-id="1691a-137">A feladatot tartalmazó meghajtók listája.</span><span class="sxs-lookup"><span data-stu-id="1691a-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="1691a-138">A kivitelezéshez tekintse meg a DRIVELIST tulajdonságainak megjegyzések szakaszát, és hozzon létre egy ujjlenyomat-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1691a-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="1691a-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1691a-139">-InputObject</span></span>
<span data-ttu-id="1691a-140">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1691a-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1691a-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="1691a-141">-LogLevel</span></span>
<span data-ttu-id="1691a-142">Azt jelzi, hogy engedélyezve van-e a hibák naplózása vagy a részletes naplózás.</span><span class="sxs-lookup"><span data-stu-id="1691a-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="1691a-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1691a-143">-Name</span></span>
<span data-ttu-id="1691a-144">Az Importálás/exportálás feladat neve.</span><span class="sxs-lookup"><span data-stu-id="1691a-144">The name of the import/export job.</span></span>

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

### <span data-ttu-id="1691a-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1691a-145">-ResourceGroupName</span></span>
<span data-ttu-id="1691a-146">Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1691a-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="1691a-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="1691a-147">-ReturnAddressCity</span></span>
<span data-ttu-id="1691a-148">A lemezmeghajtók visszatéréséhez használandó település neve.</span><span class="sxs-lookup"><span data-stu-id="1691a-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="1691a-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="1691a-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="1691a-150">A meghajtók visszaadása során használandó ország vagy régió.</span><span class="sxs-lookup"><span data-stu-id="1691a-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="1691a-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="1691a-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="1691a-152">A visszaadott meghajtók címzettje e-mail-címe.</span><span class="sxs-lookup"><span data-stu-id="1691a-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="1691a-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="1691a-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="1691a-154">A visszaadott meghajtók címzettjeinek telefonszáma.</span><span class="sxs-lookup"><span data-stu-id="1691a-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="1691a-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="1691a-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="1691a-156">A lemezmeghajtók visszatéréséhez használandó irányítószám.</span><span class="sxs-lookup"><span data-stu-id="1691a-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="1691a-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="1691a-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="1691a-158">Annak a címzettnek a neve, aki a visszatéréskor a merevlemezt fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="1691a-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="1691a-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="1691a-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="1691a-160">A meghajtók visszatéréséhez használandó állam vagy tartomány.</span><span class="sxs-lookup"><span data-stu-id="1691a-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="1691a-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="1691a-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="1691a-162">A lemezmeghajtók visszatéréséhez használandó utcanév első sora.</span><span class="sxs-lookup"><span data-stu-id="1691a-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="1691a-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="1691a-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="1691a-164">A lemezmeghajtók visszatéréséhez használandó utcanév második sora.</span><span class="sxs-lookup"><span data-stu-id="1691a-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="1691a-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="1691a-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="1691a-166">Az ügyfél számlaszáma a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="1691a-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="1691a-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="1691a-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="1691a-168">A fuvarozó neve.</span><span class="sxs-lookup"><span data-stu-id="1691a-168">The carrier's name.</span></span>

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

### <span data-ttu-id="1691a-169">-State (állami)</span><span class="sxs-lookup"><span data-stu-id="1691a-169">-State</span></span>
<span data-ttu-id="1691a-170">Ha meg van adva, akkor az értéknek a szállítás elemnek kell lennie, amely tájékoztatja az importálási/exportálási szolgáltatást, amelyet a projekthez tartozó csomag leszállított.</span><span class="sxs-lookup"><span data-stu-id="1691a-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="1691a-171">A ReturnAddress és a DeliveryPackage tulajdonságot be kell állítani az ebben a kérésben vagy egy korábbi kérésben, máskülönben a kérés meghiúsul.</span><span class="sxs-lookup"><span data-stu-id="1691a-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="1691a-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1691a-172">-SubscriptionId</span></span>
<span data-ttu-id="1691a-173">Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1691a-173">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="1691a-174">-Címke</span><span class="sxs-lookup"><span data-stu-id="1691a-174">-Tag</span></span>
<span data-ttu-id="1691a-175">A feladathoz hozzárendelni kívánt címkéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="1691a-175">Specifies the tags that will be assigned to the job</span></span>

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

### <span data-ttu-id="1691a-176">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1691a-176">-Confirm</span></span>
<span data-ttu-id="1691a-177">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1691a-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1691a-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1691a-178">-WhatIf</span></span>
<span data-ttu-id="1691a-179">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1691a-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1691a-180">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1691a-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1691a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1691a-181">CommonParameters</span></span>
<span data-ttu-id="1691a-182">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1691a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1691a-183">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1691a-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1691a-184">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1691a-184">INPUTS</span></span>

### <span data-ttu-id="1691a-185">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="1691a-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="1691a-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1691a-186">OUTPUTS</span></span>

### <span data-ttu-id="1691a-187">Microsoft. Azure. PowerShell. parancsmagok. ImportExport. modellek. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="1691a-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="1691a-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1691a-188">NOTES</span></span>

<span data-ttu-id="1691a-189">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1691a-189">ALIASES</span></span>

<span data-ttu-id="1691a-190">KOMPLEX PARAMÉTEREK TULAJDONSÁGAI</span><span class="sxs-lookup"><span data-stu-id="1691a-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1691a-191">Az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1691a-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1691a-192">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1691a-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1691a-193">DRIVELIST <IDriveStatus [] >: a feladatot tartalmazó meghajtók listája.</span><span class="sxs-lookup"><span data-stu-id="1691a-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="1691a-194">`[BitLockerKey <String>]`: A meghajtó titkosításához használt BitLocker-kulcs.</span><span class="sxs-lookup"><span data-stu-id="1691a-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="1691a-195">`[BytesSucceeded <Int64?>]`: Sikeresen átvitt bájtok a meghajtóra.</span><span class="sxs-lookup"><span data-stu-id="1691a-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="1691a-196">`[CopyStatus <String>]`: Az adatátviteli folyamat részletes állapota.</span><span class="sxs-lookup"><span data-stu-id="1691a-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="1691a-197">Ezt a mezőt addig nem adja vissza a válasz, amíg a meghajtó az átadó államban van.</span><span class="sxs-lookup"><span data-stu-id="1691a-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="1691a-198">`[DriveHeaderHash <String>]`: A meghajtó fejléc-ujjlenyomatának értéke.</span><span class="sxs-lookup"><span data-stu-id="1691a-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="1691a-199">`[DriveId <String>]`: A meghajtó hardveres sorozatszáma szóközök nélkül.</span><span class="sxs-lookup"><span data-stu-id="1691a-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="1691a-200">`[ErrorLogUri <String>]`: Egy URI, amely az adatátviteli művelethez az adattovábbítási művelethez tartozó hibát tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="1691a-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="1691a-201">`[ManifestFile <String>]`: A manifest-fájl relatív elérési útja a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="1691a-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="1691a-202">`[ManifestHash <String>]`: A manifest-fájl Base16 kódolt MD5 hash-je a meghajtón.</span><span class="sxs-lookup"><span data-stu-id="1691a-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="1691a-203">`[ManifestUri <String>]`: A Drive manifest-fájlt tartalmazó blobra mutató URI.</span><span class="sxs-lookup"><span data-stu-id="1691a-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="1691a-204">`[PercentComplete <Int32?>]`: Készültségi% a meghajtóhoz.</span><span class="sxs-lookup"><span data-stu-id="1691a-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="1691a-205">`[State <DriveState?>]`: A meghajtó jelenlegi állapota.</span><span class="sxs-lookup"><span data-stu-id="1691a-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="1691a-206">`[VerboseLogUri <String>]`: Egy URI, amely az adatátviteli művelet részletes naplóját tartalmazó blobra mutat.</span><span class="sxs-lookup"><span data-stu-id="1691a-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="1691a-207">INPUTOBJECT <IImportExportIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1691a-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1691a-208">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1691a-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1691a-209">`[JobName <String>]`: Az importálási/exportálási feladat neve.</span><span class="sxs-lookup"><span data-stu-id="1691a-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="1691a-210">`[LocationName <String>]`: A hely neve.</span><span class="sxs-lookup"><span data-stu-id="1691a-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="1691a-211">Például Nyugat-amerikai vagy westus.</span><span class="sxs-lookup"><span data-stu-id="1691a-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="1691a-212">`[ResourceGroupName <String>]`: Az erőforráscsoport neve egyedileg azonosítja az erőforráscsoportot a felhasználói előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1691a-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="1691a-213">`[SubscriptionId <String>]`: Az Azure-felhasználó előfizetési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1691a-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="1691a-214">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1691a-214">RELATED LINKS</span></span>

