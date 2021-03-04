---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 34caab92645f610ed6ed71d907639060cf0c456a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921425"
---
# <span data-ttu-id="57bdf-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="57bdf-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="57bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="57bdf-103">Konfigurálható lemezobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="57bdf-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="57bdf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57bdf-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>]
 [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-BurstingEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57bdf-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57bdf-105">DESCRIPTION</span></span>
<span data-ttu-id="57bdf-106">A **New-AzDiskConfig** parancsmag létrehoz egy konfigurálható lemezobjektumot.</span><span class="sxs-lookup"><span data-stu-id="57bdf-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="57bdf-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57bdf-107">EXAMPLES</span></span>

### <span data-ttu-id="57bdf-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="57bdf-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="57bdf-109">Az első parancs egy 5 GB-os helyi üres lemezobjektumot hoz létre Standard_LRS tárfióktípusban.</span><span class="sxs-lookup"><span data-stu-id="57bdf-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="57bdf-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="57bdf-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="57bdf-111">A második és a harmadik parancs a lemezobjektum lemeztitkosítási kulcsának és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="57bdf-112">Az utolsó parancs átveszi a lemezobjektumot, és létrehoz egy "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="57bdf-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="57bdf-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="57bdf-113">Example 2</span></span>
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

<span data-ttu-id="57bdf-114">Az első parancs helyi lemezobjektumot hoz létre a Feltöltés parancshoz.</span><span class="sxs-lookup"><span data-stu-id="57bdf-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="57bdf-115">A második parancs átveszi a lemezobjektumot, és létrehoz egy "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="57bdf-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="57bdf-116">A harmadik parancs az SAS URL-címet kapja a lemezhez.</span><span class="sxs-lookup"><span data-stu-id="57bdf-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="57bdf-117">A negyedik parancs a lemez állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="57bdf-118">Ha a lemez állapota "ReadyToUpload", a felhasználó feltölthet egy lemezt a blobtárból a lemez SAS URL-címére az AzCopy használatával.</span><span class="sxs-lookup"><span data-stu-id="57bdf-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="57bdf-119">A feltöltés során a lemez állapota "ActiveUpload" állapotba változik.</span><span class="sxs-lookup"><span data-stu-id="57bdf-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="57bdf-120">Az utolsó parancs visszavonja az SAS URL-cím lemezelérését.</span><span class="sxs-lookup"><span data-stu-id="57bdf-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="57bdf-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="57bdf-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="57bdf-122">Hozzon létre egy lemezt a Megosztott gyűjtemény képverzióból.</span><span class="sxs-lookup"><span data-stu-id="57bdf-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="57bdf-123">Az azonosító a galéria megosztott képverziójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="57bdf-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="57bdf-124">Lunra csak akkor van szükség, ha a forrás egy adatlemez.</span><span class="sxs-lookup"><span data-stu-id="57bdf-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="57bdf-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57bdf-125">PARAMETERS</span></span>

### <span data-ttu-id="57bdf-126">-TetszetvesEnabled</span><span class="sxs-lookup"><span data-stu-id="57bdf-126">-BurstingEnabled</span></span>
<span data-ttu-id="57bdf-127">Lehetővé teszi, hogy a program a kiépített teljesítménycélon túlra sorozatos sorozatot létesítsen a lemezen.</span><span class="sxs-lookup"><span data-stu-id="57bdf-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="57bdf-128">A sorozatfelvétel alapértelmezés szerint le van tiltva.</span><span class="sxs-lookup"><span data-stu-id="57bdf-128">Bursting is disabled by default.</span></span> <span data-ttu-id="57bdf-129">Az Ultra lemezre nem érvényes.</span><span class="sxs-lookup"><span data-stu-id="57bdf-129">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="57bdf-130">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="57bdf-130">-CreateOption</span></span>
<span data-ttu-id="57bdf-131">Azt adja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépben egy platformról vagy egy felhasználói képről, létrehoz-e egy üres lemezt, vagy csatol-e egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="57bdf-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="57bdf-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57bdf-132">-DefaultProfile</span></span>
<span data-ttu-id="57bdf-133">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57bdf-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57bdf-134">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="57bdf-134">-DiskAccessId</span></span>
<span data-ttu-id="57bdf-135">Beállítja ARM a DiskAccess erőforrás azonosítóját a privát végpontok használatának beállításával.</span><span class="sxs-lookup"><span data-stu-id="57bdf-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="57bdf-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="57bdf-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="57bdf-137">A lemezen található lemeztitkosítási kulcsobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-137">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="57bdf-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="57bdf-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="57bdf-139">Megadja annak a lemeztitkosítási készletnek az erőforrás-azonosítóját, amely a nyugta titkosítás engedélyezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="57bdf-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="57bdf-140">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="57bdf-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="57bdf-141">Az összes olyan VM-hez engedélyezett IOPS-fájlok száma, amelyek a megosztott lemezhez ReadOnly-ként lesznek rögzítve.</span><span class="sxs-lookup"><span data-stu-id="57bdf-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="57bdf-142">Egy művelet 4 és 256 bájt közötti átvitelt tud.</span><span class="sxs-lookup"><span data-stu-id="57bdf-142">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="57bdf-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="57bdf-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="57bdf-144">Az ehhez a lemezhez engedélyezett IOPS-k száma; csak az UltraSSD-lemezhez van beállítva.</span><span class="sxs-lookup"><span data-stu-id="57bdf-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="57bdf-145">Egy művelet 4 és 256 bájt közötti átvitelt tud.</span><span class="sxs-lookup"><span data-stu-id="57bdf-145">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="57bdf-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="57bdf-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="57bdf-147">"description": "Az a teljes átviteli sebesség (MBps), amely az összes olyan VM-hez engedélyezett, amely a megosztott lemezt ReadOnly-ként rögzíti.</span><span class="sxs-lookup"><span data-stu-id="57bdf-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="57bdf-148">A MBps másodpercenként több millió bájtot jelent – a MB itt a 10-eshatalmak ISO-ként való meghatalmazását használja.</span><span class="sxs-lookup"><span data-stu-id="57bdf-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="57bdf-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="57bdf-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="57bdf-150">A lemezhez engedélyezett sávszélesség; csak az UltraSSD-lemezhez van beállítva.</span><span class="sxs-lookup"><span data-stu-id="57bdf-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="57bdf-151">A MBps másodpercenként több millió bájtot jelent – a MB itt a 10-eshatalmak ISO-ként való meghatalmazását használja.</span><span class="sxs-lookup"><span data-stu-id="57bdf-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="57bdf-152">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="57bdf-152">-DiskSizeGB</span></span>
<span data-ttu-id="57bdf-153">A lemez mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="57bdf-153">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="57bdf-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="57bdf-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="57bdf-155">Engedélyezze a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="57bdf-155">Enable encryption settings.</span></span>

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

### <span data-ttu-id="57bdf-156">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="57bdf-156">-EncryptionType</span></span>
<span data-ttu-id="57bdf-157">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="57bdf-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="57bdf-158">A rendelkezésre álló értékek: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="57bdf-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="57bdf-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="57bdf-159">-GalleryImageReference</span></span>
<span data-ttu-id="57bdf-160">A GalleryImageReference objektum.</span><span class="sxs-lookup"><span data-stu-id="57bdf-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="57bdf-161">Galériaképből való létrehozás kötelező.</span><span class="sxs-lookup"><span data-stu-id="57bdf-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="57bdf-162">Az azonosító annak a megosztott ARM képverziónak a ARM azonosítója lesz, amelyből létre kell hoznia egy lemezt.</span><span class="sxs-lookup"><span data-stu-id="57bdf-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="57bdf-163">Lunra van szükség, ha a másolat forrása a galériakép egyik adatlemeze; ha null, a rendszer a kép operációsrendszer-lemezét másolja.</span><span class="sxs-lookup"><span data-stu-id="57bdf-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="57bdf-164">-HyperVGeneráció</span><span class="sxs-lookup"><span data-stu-id="57bdf-164">-HyperVGeneration</span></span>
<span data-ttu-id="57bdf-165">A virtuális gép hipervizor-generálása.</span><span class="sxs-lookup"><span data-stu-id="57bdf-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="57bdf-166">Csak operációs rendszer lemezei esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="57bdf-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="57bdf-167">Az engedélyezett értékek a V1 és a V2.</span><span class="sxs-lookup"><span data-stu-id="57bdf-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="57bdf-168">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="57bdf-168">-ImageReference</span></span>
<span data-ttu-id="57bdf-169">A lemez képhivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-169">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="57bdf-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="57bdf-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="57bdf-171">A lemez kulcstitkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-171">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="57bdf-172">-Location</span><span class="sxs-lookup"><span data-stu-id="57bdf-172">-Location</span></span>
<span data-ttu-id="57bdf-173">Megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="57bdf-173">Specifies a location.</span></span>

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

### <span data-ttu-id="57bdf-174">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="57bdf-174">-LogicalSectorSize</span></span>
<span data-ttu-id="57bdf-175">Logikai ágazat mérete bájtban az Ultra lemez esetén.</span><span class="sxs-lookup"><span data-stu-id="57bdf-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="57bdf-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="57bdf-176">-MaxSharesCount</span></span>
<span data-ttu-id="57bdf-177">A lemezhez egyszerre csatolhat virtuális gépek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="57bdf-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="57bdf-178">Az egynél nagyobb érték olyan lemez, amely egyszerre több virtuális gépre is fel lehet szerelve.</span><span class="sxs-lookup"><span data-stu-id="57bdf-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="57bdf-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="57bdf-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="57bdf-180">A hálózati hozzáférési házirend határozza meg a hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="57bdf-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="57bdf-181">Lehetséges értékek: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="57bdf-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="57bdf-182">-OsType</span><span class="sxs-lookup"><span data-stu-id="57bdf-182">-OsType</span></span>
<span data-ttu-id="57bdf-183">Az operációs rendszer típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-183">Specifies the OS type.</span></span>

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

### <span data-ttu-id="57bdf-184">-SkuName</span><span class="sxs-lookup"><span data-stu-id="57bdf-184">-SkuName</span></span>
<span data-ttu-id="57bdf-185">A tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="57bdf-186">A rendelkezésre álló értékek a következő értékek: Standard_LRS, Premium_LRS, StandardSSD_LRS és UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="57bdf-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="57bdf-187">UltraSSD_LRS a CreateOption paraméterhez csak üres érték használható.</span><span class="sxs-lookup"><span data-stu-id="57bdf-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="57bdf-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="57bdf-188">-SourceResourceId</span></span>
<span data-ttu-id="57bdf-189">A forráserőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="57bdf-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="57bdf-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="57bdf-190">-SourceUri</span></span>
<span data-ttu-id="57bdf-191">A forrás Uri-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="57bdf-192">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="57bdf-192">-StorageAccountId</span></span>
<span data-ttu-id="57bdf-193">Megadja a tárfiók azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="57bdf-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="57bdf-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="57bdf-194">-Tag</span></span>
<span data-ttu-id="57bdf-195">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="57bdf-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="57bdf-196">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="57bdf-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="57bdf-197">-Tier</span><span class="sxs-lookup"><span data-stu-id="57bdf-197">-Tier</span></span>
<span data-ttu-id="57bdf-198">A lemez teljesítményrétege.</span><span class="sxs-lookup"><span data-stu-id="57bdf-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="57bdf-199">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="57bdf-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="57bdf-200">A feltöltés tartalmának mérete, beleértve a VHD élőlábat is, amikor a CreateOption a Upload.</span><span class="sxs-lookup"><span data-stu-id="57bdf-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="57bdf-201">Ennek az értéknek 20972032 (20 MiB + 512 bájt a VHD élőlábhoz) és 35183298347520 bájtnak (32 TiB + 512 bájt a VHD élőlábhoz) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="57bdf-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="57bdf-202">-Zone</span><span class="sxs-lookup"><span data-stu-id="57bdf-202">-Zone</span></span>
<span data-ttu-id="57bdf-203">A Lemez logikai zónalistát adja meg.</span><span class="sxs-lookup"><span data-stu-id="57bdf-203">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="57bdf-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57bdf-204">-Confirm</span></span>
<span data-ttu-id="57bdf-205">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="57bdf-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57bdf-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57bdf-206">-WhatIf</span></span>
<span data-ttu-id="57bdf-207">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="57bdf-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57bdf-208">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="57bdf-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57bdf-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57bdf-209">CommonParameters</span></span>
<span data-ttu-id="57bdf-210">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57bdf-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57bdf-211">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57bdf-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57bdf-212">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57bdf-212">INPUTS</span></span>

### <span data-ttu-id="57bdf-213">System.String</span><span class="sxs-lookup"><span data-stu-id="57bdf-213">System.String</span></span>

### <span data-ttu-id="57bdf-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="57bdf-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="57bdf-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="57bdf-215">System.Int32</span></span>

### <span data-ttu-id="57bdf-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="57bdf-216">System.String[]</span></span>

### <span data-ttu-id="57bdf-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="57bdf-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="57bdf-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="57bdf-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="57bdf-219">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57bdf-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="57bdf-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="57bdf-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="57bdf-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="57bdf-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="57bdf-222">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57bdf-222">OUTPUTS</span></span>

### <span data-ttu-id="57bdf-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="57bdf-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="57bdf-224">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57bdf-224">NOTES</span></span>

## <span data-ttu-id="57bdf-225">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57bdf-225">RELATED LINKS</span></span>
