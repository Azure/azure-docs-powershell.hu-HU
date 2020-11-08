---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 7a8c4bc3b875cb9072386784fe1c06730be89405
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011474"
---
# <span data-ttu-id="8baea-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="8baea-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="8baea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8baea-102">SYNOPSIS</span></span>
<span data-ttu-id="8baea-103">Konfigurálható lemezkezelő-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8baea-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="8baea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8baea-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8baea-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8baea-105">DESCRIPTION</span></span>
<span data-ttu-id="8baea-106">A **New-AzDiskConfig** parancsmag létrehoz egy konfigurálható Disk-objektumot.</span><span class="sxs-lookup"><span data-stu-id="8baea-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="8baea-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8baea-107">EXAMPLES</span></span>

### <span data-ttu-id="8baea-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8baea-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="8baea-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="8baea-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="8baea-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="8baea-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="8baea-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="8baea-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="8baea-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="8baea-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8baea-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="8baea-114">Az első parancs létrehoz egy helyi lemez-objektumot a feltöltéshez.</span><span class="sxs-lookup"><span data-stu-id="8baea-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="8baea-115">A második parancs átveszi a Disk objektumot, és létrehoz egy "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="8baea-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="8baea-116">A harmadik parancs megkapja a biztonsági társítás URL-címét.</span><span class="sxs-lookup"><span data-stu-id="8baea-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="8baea-117">A negyedik parancs a lemez állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="8baea-118">Ha a lemez állapota "ReadyToUpload", a felhasználó feltöltheti a blob-tárolóról a lemezeket a AzCopy segítségével.</span><span class="sxs-lookup"><span data-stu-id="8baea-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="8baea-119">A feltöltés során a lemez állapota "ActiveUpload" értékre változik.</span><span class="sxs-lookup"><span data-stu-id="8baea-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="8baea-120">Az utolsó parancs visszavonja a biztonsági társítás URL-címének elérését.</span><span class="sxs-lookup"><span data-stu-id="8baea-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="8baea-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="8baea-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="8baea-122">Lemez létrehozása egy megosztott gyűjtemény képének verziójában.</span><span class="sxs-lookup"><span data-stu-id="8baea-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="8baea-123">Azonosító – a megosztott tár képének azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8baea-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="8baea-124">A logikai egységnek csak akkor van szüksége, ha a forrás adatlemez.</span><span class="sxs-lookup"><span data-stu-id="8baea-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="8baea-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8baea-125">PARAMETERS</span></span>

### <span data-ttu-id="8baea-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="8baea-126">-CreateOption</span></span>
<span data-ttu-id="8baea-127">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="8baea-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8baea-128">-DefaultProfile</span></span>
<span data-ttu-id="8baea-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8baea-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-130">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8baea-130">-DiskEncryptionKey</span></span>
<span data-ttu-id="8baea-131">A lemez titkosítási kulcs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-131">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-132">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8baea-132">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8baea-133">A titkosításnak a REST szolgáltatáshoz való engedélyezéséhez használt titkosító erőforrás azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-133">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-134">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="8baea-134">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="8baea-135">Annak a IOPS a teljes száma, amelyet az összes VMs-meghajtón meg kell adni az írásvédett példányban.</span><span class="sxs-lookup"><span data-stu-id="8baea-135">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="8baea-136">Egy művelet átadható a 4k és a 256k között.</span><span class="sxs-lookup"><span data-stu-id="8baea-136">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-137">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="8baea-137">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="8baea-138">A lemezre engedélyezett IOPS száma; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="8baea-138">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="8baea-139">Egy művelet átadható a 4k és a 256k között.</span><span class="sxs-lookup"><span data-stu-id="8baea-139">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-140">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="8baea-140">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="8baea-141">"Description": "a teljes átviteli sebesség (Mbit/s), amelyet a rendszer minden VMs-meghajtón használhat ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="8baea-141">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="8baea-142">MBps: a 10 MB/s sebességű bájtok száma itt az ISO-jelölést használja, a 10-es hatáskörökkel.</span><span class="sxs-lookup"><span data-stu-id="8baea-142">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-143">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="8baea-143">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="8baea-144">A lemezre engedélyezett sávszélesség; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="8baea-144">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="8baea-145">MBps: a 10 MB/s sebességű bájtok száma itt az ISO-jelölést használja, a 10-es hatáskörökkel.</span><span class="sxs-lookup"><span data-stu-id="8baea-145">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-146">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="8baea-146">-DiskSizeGB</span></span>
<span data-ttu-id="8baea-147">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="8baea-147">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-148">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="8baea-148">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="8baea-149">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="8baea-149">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-150">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="8baea-150">-EncryptionType</span></span>
<span data-ttu-id="8baea-151">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="8baea-151">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="8baea-152">A rendelkezésre álló értékek a következők: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="8baea-152">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-153">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="8baea-153">-GalleryImageReference</span></span>
<span data-ttu-id="8baea-154">A GalleryImageReference objektum.</span><span class="sxs-lookup"><span data-stu-id="8baea-154">The GalleryImageReference object.</span></span>  <span data-ttu-id="8baea-155">Szükséges, ha gyűjteményből származó képet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8baea-155">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="8baea-156">Az azonosító annak a megosztott hasáb-képfájlnak a karja azonosítója lesz, amelyből lemez hozható létre.</span><span class="sxs-lookup"><span data-stu-id="8baea-156">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="8baea-157">A logikai egységekre akkor van szükség, ha a másolat forrása a gyűjteményben lévő adatlemezek egyike. Ha NULL, a program a kép operációs rendszerű lemezét másolja.</span><span class="sxs-lookup"><span data-stu-id="8baea-157">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-158">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="8baea-158">-HyperVGeneration</span></span>
<span data-ttu-id="8baea-159">A virtuális gép hypervisor-generációja.</span><span class="sxs-lookup"><span data-stu-id="8baea-159">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="8baea-160">Csak az operációsrendszer-lemezekre érvényes.</span><span class="sxs-lookup"><span data-stu-id="8baea-160">Applicable to OS disks only.</span></span>  <span data-ttu-id="8baea-161">A megengedett értékek a v1 és a v2.</span><span class="sxs-lookup"><span data-stu-id="8baea-161">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-162">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="8baea-162">-ImageReference</span></span>
<span data-ttu-id="8baea-163">A kép hivatkozását adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="8baea-163">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-164">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8baea-164">-KeyEncryptionKey</span></span>
<span data-ttu-id="8baea-165">A kulcs titkosítási kulcsát adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="8baea-165">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-166">-Hely</span><span class="sxs-lookup"><span data-stu-id="8baea-166">-Location</span></span>
<span data-ttu-id="8baea-167">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-167">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-168">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="8baea-168">-MaxSharesCount</span></span>
<span data-ttu-id="8baea-169">A merevlemezhez egyidejűleg használható VMs-tartomány maximális száma.</span><span class="sxs-lookup"><span data-stu-id="8baea-169">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="8baea-170">Az értéknél nagyobb érték azt jelzi, hogy egyszerre több VMs-eszközön lehet csatlakoztatni egy lemezt.</span><span class="sxs-lookup"><span data-stu-id="8baea-170">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-171">-OsType</span><span class="sxs-lookup"><span data-stu-id="8baea-171">-OsType</span></span>
<span data-ttu-id="8baea-172">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-172">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8baea-173">-SkuName</span></span>
<span data-ttu-id="8baea-174">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="8baea-174">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="8baea-175">A rendelkezésre álló értékek az Standard_LRS, a Premium_LRS, a StandardSSD_LRS és a UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="8baea-175">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="8baea-176">A UltraSSD_LRS csak a CreateOption paraméter üres értékével használható.</span><span class="sxs-lookup"><span data-stu-id="8baea-176">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-177">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="8baea-177">-SourceResourceId</span></span>
<span data-ttu-id="8baea-178">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-178">Specifies the  source resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-179">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="8baea-179">-SourceUri</span></span>
<span data-ttu-id="8baea-180">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-180">Specifies the source Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-181">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8baea-181">-StorageAccountId</span></span>
<span data-ttu-id="8baea-182">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-182">Specifies the storage account ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-183">-Címke</span><span class="sxs-lookup"><span data-stu-id="8baea-183">-Tag</span></span>
<span data-ttu-id="8baea-184">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="8baea-184">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8baea-185">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="8baea-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-186">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="8baea-186">-UploadSizeInBytes</span></span>
<span data-ttu-id="8baea-187">A feltöltés CreateOption a VHD-láblécet tartalmazó feltöltés tartalmának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-187">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="8baea-188">Ennek az értéknek a 20972032-as (20 MiB + 512 bájtnál a VHD-lábléchez) és az 35183298347520 bájt (32 TiB + 512 bájt a VHD-láblécben) között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="8baea-188">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-189">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="8baea-189">-Zone</span></span>
<span data-ttu-id="8baea-190">A lemez logikai zóna-listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8baea-190">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8baea-191">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8baea-191">-Confirm</span></span>
<span data-ttu-id="8baea-192">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8baea-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8baea-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8baea-193">-WhatIf</span></span>
<span data-ttu-id="8baea-194">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8baea-194">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8baea-195">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8baea-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8baea-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8baea-196">CommonParameters</span></span>
<span data-ttu-id="8baea-197">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8baea-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8baea-198">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8baea-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8baea-199">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8baea-199">INPUTS</span></span>

### <span data-ttu-id="8baea-200">System. String</span><span class="sxs-lookup"><span data-stu-id="8baea-200">System.String</span></span>

### <span data-ttu-id="8baea-201">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8baea-201">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8baea-202">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8baea-202">System.Int32</span></span>

### <span data-ttu-id="8baea-203">System. string []</span><span class="sxs-lookup"><span data-stu-id="8baea-203">System.String[]</span></span>

### <span data-ttu-id="8baea-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8baea-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8baea-205">Microsoft. Azure. Management. kiszámítás. models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="8baea-205">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="8baea-206">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8baea-206">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8baea-207">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="8baea-207">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="8baea-208">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="8baea-208">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="8baea-209">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8baea-209">OUTPUTS</span></span>

### <span data-ttu-id="8baea-210">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="8baea-210">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="8baea-211">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8baea-211">NOTES</span></span>

## <span data-ttu-id="8baea-212">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8baea-212">RELATED LINKS</span></span>
