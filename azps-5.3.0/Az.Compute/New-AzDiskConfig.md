---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477738"
---
# <span data-ttu-id="db612-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="db612-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="db612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db612-102">SYNOPSIS</span></span>
<span data-ttu-id="db612-103">Konfigurálható lemezobjektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="db612-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="db612-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="db612-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>]
 [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db612-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="db612-105">DESCRIPTION</span></span>
<span data-ttu-id="db612-106">A **New-AzDiskConfig** parancsmag létrehoz egy konfigurálható lemezobjektumot.</span><span class="sxs-lookup"><span data-stu-id="db612-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="db612-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="db612-107">EXAMPLES</span></span>

### <span data-ttu-id="db612-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="db612-108">Example 1</span></span>
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

<span data-ttu-id="db612-109">Az első parancs egy 5 GB-os helyi üres lemezobjektumot hoz létre Standard_LRS tárfióktípusban.</span><span class="sxs-lookup"><span data-stu-id="db612-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="db612-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="db612-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="db612-111">A második és a harmadik parancs a lemezobjektum lemeztitkosítási kulcsának és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="db612-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="db612-112">Az utolsó parancs átveszi a lemezobjektumot, és létrehoz egy "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="db612-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="db612-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="db612-113">Example 2</span></span>
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

<span data-ttu-id="db612-114">Az első parancs helyi lemezobjektumot hoz létre a Feltöltés parancshoz.</span><span class="sxs-lookup"><span data-stu-id="db612-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="db612-115">A második parancs átveszi a lemezobjektumot, és létrehoz egy "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="db612-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="db612-116">A harmadik parancs a lemez SAS URL-címét kapja.</span><span class="sxs-lookup"><span data-stu-id="db612-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="db612-117">A negyedik parancs a lemez állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="db612-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="db612-118">Ha a lemez állapota "ReadyToUpload", a felhasználó feltölthet egy lemezt a blobtárból a lemez SAS URL-címére az AzCopy használatával.</span><span class="sxs-lookup"><span data-stu-id="db612-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="db612-119">A feltöltés során a lemez állapota "ActiveUpload" állapotba változik.</span><span class="sxs-lookup"><span data-stu-id="db612-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="db612-120">Az utolsó parancs visszavonja az SAS URL-cím lemezelérését.</span><span class="sxs-lookup"><span data-stu-id="db612-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="db612-121">3. példa</span><span class="sxs-lookup"><span data-stu-id="db612-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="db612-122">Hozzon létre egy lemezt a Megosztott gyűjtemény képverzióból.</span><span class="sxs-lookup"><span data-stu-id="db612-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="db612-123">Az azonosító a galéria megosztott képverziójának azonosítója.</span><span class="sxs-lookup"><span data-stu-id="db612-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="db612-124">Lunra csak akkor van szükség, ha a forrás egy adatlemez.</span><span class="sxs-lookup"><span data-stu-id="db612-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="db612-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db612-125">PARAMETERS</span></span>

### <span data-ttu-id="db612-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="db612-126">-CreateOption</span></span>
<span data-ttu-id="db612-127">Azt adja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépben egy platformról vagy egy felhasználói képről, létrehoz-e egy üres lemezt, vagy csatol-e egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="db612-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="db612-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db612-128">-DefaultProfile</span></span>
<span data-ttu-id="db612-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db612-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db612-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="db612-130">-DiskAccessId</span></span>
<span data-ttu-id="db612-131">Beállítja ARM a DiskAccess erőforrás azonosítóját a privát végpontok használatának beállításával.</span><span class="sxs-lookup"><span data-stu-id="db612-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="db612-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="db612-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="db612-133">A lemezen található lemeztitkosítási kulcsobjektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="db612-133">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="db612-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="db612-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="db612-135">Megadja annak a lemeztitkosítási készletnek az erőforrás-azonosítóját, amely a nyugta titkosítás engedélyezéséhez használható.</span><span class="sxs-lookup"><span data-stu-id="db612-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="db612-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="db612-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="db612-137">Az összes olyan VM-hez engedélyezett IOPS-fájlok száma, amelyek a megosztott lemezhez ReadOnly-ként vannak rögzítve.</span><span class="sxs-lookup"><span data-stu-id="db612-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="db612-138">Egy művelet 4 és 256 bájt közötti átvitelt tud.</span><span class="sxs-lookup"><span data-stu-id="db612-138">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="db612-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="db612-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="db612-140">Az ehhez a lemezhez engedélyezett IOPS-k száma; csak az UltraSSD-lemezhez van beállítva.</span><span class="sxs-lookup"><span data-stu-id="db612-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="db612-141">Egy művelet 4 és 256 bájt közötti átvitelt tud.</span><span class="sxs-lookup"><span data-stu-id="db612-141">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="db612-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="db612-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="db612-143">"description": "Az a teljes átviteli sebesség (MBps), amely az összes olyan VM-hez engedélyezett, amely a megosztott lemezt ReadOnly-ként rögzíti.</span><span class="sxs-lookup"><span data-stu-id="db612-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="db612-144">A MBps másodpercenként több millió bájtot jelent – a MB itt a 10-eshatalmak ISO-ként való meghatalmazását használja.</span><span class="sxs-lookup"><span data-stu-id="db612-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="db612-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="db612-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="db612-146">A lemezhez engedélyezett sávszélesség; csak az UltraSSD-lemezhez van beállítva.</span><span class="sxs-lookup"><span data-stu-id="db612-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="db612-147">A MBps másodpercenként több millió bájtot jelent – a MB itt a 10-eshatalmak ISO-ként való meghatalmazását használja.</span><span class="sxs-lookup"><span data-stu-id="db612-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="db612-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="db612-148">-DiskSizeGB</span></span>
<span data-ttu-id="db612-149">A lemez mérete GB-ban.</span><span class="sxs-lookup"><span data-stu-id="db612-149">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="db612-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="db612-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="db612-151">Engedélyezze a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="db612-151">Enable encryption settings.</span></span>

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

### <span data-ttu-id="db612-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="db612-152">-EncryptionType</span></span>
<span data-ttu-id="db612-153">A lemez adatainak titkosításához használt kulcs típusa.</span><span class="sxs-lookup"><span data-stu-id="db612-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="db612-154">A rendelkezésre álló értékek: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="db612-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="db612-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="db612-155">-GalleryImageReference</span></span>
<span data-ttu-id="db612-156">A GalleryImageReference objektum.</span><span class="sxs-lookup"><span data-stu-id="db612-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="db612-157">Galériaképből való létrehozás kötelező.</span><span class="sxs-lookup"><span data-stu-id="db612-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="db612-158">Az azonosító annak a megosztott ARM képverziónak a ARM azonosítója lesz, amelyből létre kell hoznia egy lemezt.</span><span class="sxs-lookup"><span data-stu-id="db612-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="db612-159">Lunra van szükség, ha a másolat forrása a képtárban lévő adatlemezek egyike; ha null, a rendszer a kép operációsrendszer-lemezét másolja.</span><span class="sxs-lookup"><span data-stu-id="db612-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="db612-160">-HyperVGeneráció</span><span class="sxs-lookup"><span data-stu-id="db612-160">-HyperVGeneration</span></span>
<span data-ttu-id="db612-161">A virtuális gép hipervizor-generálása.</span><span class="sxs-lookup"><span data-stu-id="db612-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="db612-162">Csak operációs rendszer lemezei esetén érvényes.</span><span class="sxs-lookup"><span data-stu-id="db612-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="db612-163">Az engedélyezett értékek a V1 és a V2.</span><span class="sxs-lookup"><span data-stu-id="db612-163">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="db612-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="db612-164">-ImageReference</span></span>
<span data-ttu-id="db612-165">A lemez képhivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="db612-165">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="db612-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="db612-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="db612-167">A lemez kulcstitkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="db612-167">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="db612-168">-Location</span><span class="sxs-lookup"><span data-stu-id="db612-168">-Location</span></span>
<span data-ttu-id="db612-169">Megadja a helyet.</span><span class="sxs-lookup"><span data-stu-id="db612-169">Specifies a location.</span></span>

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

### <span data-ttu-id="db612-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="db612-170">-LogicalSectorSize</span></span>
<span data-ttu-id="db612-171">Logikai ágazat mérete bájtban az Ultra lemez esetén.</span><span class="sxs-lookup"><span data-stu-id="db612-171">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="db612-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="db612-172">-MaxSharesCount</span></span>
<span data-ttu-id="db612-173">A lemezhez egyszerre csatolhat virtuális gépek maximális száma.</span><span class="sxs-lookup"><span data-stu-id="db612-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="db612-174">Az egynél nagyobb érték olyan lemez, amely egyszerre több virtuális gépre is fel lehet szerelve.</span><span class="sxs-lookup"><span data-stu-id="db612-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="db612-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="db612-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="db612-176">A hálózati hozzáférési házirend határozza meg a hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="db612-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="db612-177">Lehetséges értékek: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="db612-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="db612-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="db612-178">-OsType</span></span>
<span data-ttu-id="db612-179">Az operációs rendszer típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="db612-179">Specifies the OS type.</span></span>

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

### <span data-ttu-id="db612-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="db612-180">-SkuName</span></span>
<span data-ttu-id="db612-181">A tárfiók termékváltozatnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="db612-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="db612-182">A rendelkezésre álló értékek Standard_LRS, Premium_LRS, StandardSSD_LRS és UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="db612-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="db612-183">UltraSSD_LRS a CreateOption paraméterhez csak üres érték használható.</span><span class="sxs-lookup"><span data-stu-id="db612-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="db612-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="db612-184">-SourceResourceId</span></span>
<span data-ttu-id="db612-185">A forráserőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="db612-185">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="db612-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="db612-186">-SourceUri</span></span>
<span data-ttu-id="db612-187">A forrás Uri-t adja meg.</span><span class="sxs-lookup"><span data-stu-id="db612-187">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="db612-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="db612-188">-StorageAccountId</span></span>
<span data-ttu-id="db612-189">Megadja a tárfiók azonosítóját.</span><span class="sxs-lookup"><span data-stu-id="db612-189">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="db612-190">-Tag</span><span class="sxs-lookup"><span data-stu-id="db612-190">-Tag</span></span>
<span data-ttu-id="db612-191">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="db612-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="db612-192">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="db612-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="db612-193">-Tier</span><span class="sxs-lookup"><span data-stu-id="db612-193">-Tier</span></span>
<span data-ttu-id="db612-194">A lemez teljesítményrétege.</span><span class="sxs-lookup"><span data-stu-id="db612-194">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="db612-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="db612-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="db612-196">A feltöltés tartalmának mérete, beleértve a VHD élőlábat is, amikor a CreateOption a Upload.</span><span class="sxs-lookup"><span data-stu-id="db612-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="db612-197">Ennek az értéknek 20972032 (20 MiB + 512 bájt a VHD élőlábhoz) és 35183298347520 bájtnak (32 TiB + 512 bájt a VHD élőlábhoz) kell lennie.</span><span class="sxs-lookup"><span data-stu-id="db612-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="db612-198">-Zone</span><span class="sxs-lookup"><span data-stu-id="db612-198">-Zone</span></span>
<span data-ttu-id="db612-199">A Lemez logikai zónalistát adja meg.</span><span class="sxs-lookup"><span data-stu-id="db612-199">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="db612-200">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db612-200">-Confirm</span></span>
<span data-ttu-id="db612-201">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="db612-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db612-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db612-202">-WhatIf</span></span>
<span data-ttu-id="db612-203">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="db612-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db612-204">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db612-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db612-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db612-205">CommonParameters</span></span>
<span data-ttu-id="db612-206">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db612-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db612-207">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db612-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db612-208">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db612-208">INPUTS</span></span>

### <span data-ttu-id="db612-209">System.String</span><span class="sxs-lookup"><span data-stu-id="db612-209">System.String</span></span>

### <span data-ttu-id="db612-210">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0,0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="db612-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="db612-211">System.Int32</span><span class="sxs-lookup"><span data-stu-id="db612-211">System.Int32</span></span>

### <span data-ttu-id="db612-212">System.String[]</span><span class="sxs-lookup"><span data-stu-id="db612-212">System.String[]</span></span>

### <span data-ttu-id="db612-213">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="db612-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="db612-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="db612-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="db612-215">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="db612-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="db612-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="db612-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="db612-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="db612-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="db612-218">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db612-218">OUTPUTS</span></span>

### <span data-ttu-id="db612-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="db612-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="db612-220">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="db612-220">NOTES</span></span>

## <span data-ttu-id="db612-221">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db612-221">RELATED LINKS</span></span>
