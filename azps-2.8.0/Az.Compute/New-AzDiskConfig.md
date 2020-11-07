---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: c37ed947441789951d8523f38e7950ad6d9d2066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667385"
---
# <span data-ttu-id="c035e-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="c035e-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="c035e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c035e-102">SYNOPSIS</span></span>
<span data-ttu-id="c035e-103">Konfigurálható lemezkezelő-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c035e-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="c035e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c035e-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c035e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c035e-105">DESCRIPTION</span></span>
<span data-ttu-id="c035e-106">A **New-AzDiskConfig** parancsmag létrehoz egy konfigurálható Disk-objektumot.</span><span class="sxs-lookup"><span data-stu-id="c035e-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="c035e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c035e-107">EXAMPLES</span></span>

### <span data-ttu-id="c035e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c035e-108">Example 1</span></span>
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

<span data-ttu-id="c035e-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="c035e-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="c035e-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="c035e-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="c035e-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="c035e-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="c035e-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c035e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c035e-113">Example 2</span></span>
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

<span data-ttu-id="c035e-114">Az első parancs létrehoz egy helyi lemez-objektumot a feltöltéshez.</span><span class="sxs-lookup"><span data-stu-id="c035e-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="c035e-115">A második parancs átveszi a Disk objektumot, és létrehoz egy "Disk01" nevű lemezt az "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="c035e-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="c035e-116">A harmadik parancs megkapja a biztonsági társítás URL-címét.</span><span class="sxs-lookup"><span data-stu-id="c035e-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="c035e-117">A negyedik parancs a lemez állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="c035e-118">Ha a lemez állapota "ReadyToUpload", a felhasználó feltöltheti a blob-tárolóról a lemezeket a AzCopy segítségével.</span><span class="sxs-lookup"><span data-stu-id="c035e-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="c035e-119">A feltöltés során a lemez állapota "ActiveUpload" értékre változik.</span><span class="sxs-lookup"><span data-stu-id="c035e-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="c035e-120">Az utolsó parancs visszavonja a biztonsági társítás URL-címének elérését.</span><span class="sxs-lookup"><span data-stu-id="c035e-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="c035e-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c035e-121">PARAMETERS</span></span>

### <span data-ttu-id="c035e-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="c035e-122">-CreateOption</span></span>
<span data-ttu-id="c035e-123">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="c035e-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="c035e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c035e-124">-DefaultProfile</span></span>
<span data-ttu-id="c035e-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c035e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c035e-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c035e-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="c035e-127">A lemez titkosítási kulcs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="c035e-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="c035e-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="c035e-129">A lemezre engedélyezett IOPS száma; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="c035e-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="c035e-130">Egy művelet átadható a 4k és a 256k között.</span><span class="sxs-lookup"><span data-stu-id="c035e-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="c035e-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="c035e-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="c035e-132">A lemezre engedélyezett sávszélesség; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="c035e-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="c035e-133">MBps: a 10 MB/s sebességű bájtok száma itt az ISO-jelölést használja, a 10-es hatáskörökkel.</span><span class="sxs-lookup"><span data-stu-id="c035e-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="c035e-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c035e-134">-DiskSizeGB</span></span>
<span data-ttu-id="c035e-135">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="c035e-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="c035e-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="c035e-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="c035e-137">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="c035e-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="c035e-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="c035e-138">-HyperVGeneration</span></span>
<span data-ttu-id="c035e-139">A virtuális gép hypervisor-generációja.</span><span class="sxs-lookup"><span data-stu-id="c035e-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="c035e-140">Csak az operációsrendszer-lemezekre érvényes.</span><span class="sxs-lookup"><span data-stu-id="c035e-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="c035e-141">A megengedett értékek a v1 és a v2.</span><span class="sxs-lookup"><span data-stu-id="c035e-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="c035e-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="c035e-142">-ImageReference</span></span>
<span data-ttu-id="c035e-143">A kép hivatkozását adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="c035e-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="c035e-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c035e-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="c035e-145">A kulcs titkosítási kulcsát adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="c035e-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="c035e-146">-Hely</span><span class="sxs-lookup"><span data-stu-id="c035e-146">-Location</span></span>
<span data-ttu-id="c035e-147">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-147">Specifies a location.</span></span>

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

### <span data-ttu-id="c035e-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="c035e-148">-OsType</span></span>
<span data-ttu-id="c035e-149">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="c035e-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c035e-150">-SkuName</span></span>
<span data-ttu-id="c035e-151">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="c035e-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="c035e-152">A rendelkezésre álló értékek az Standard_LRS, a Premium_LRS, a StandardSSD_LRS és a UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="c035e-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="c035e-153">A UltraSSD_LRS csak a CreateOption paraméter üres értékével használható.</span><span class="sxs-lookup"><span data-stu-id="c035e-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="c035e-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="c035e-154">-SourceResourceId</span></span>
<span data-ttu-id="c035e-155">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="c035e-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="c035e-156">-SourceUri</span></span>
<span data-ttu-id="c035e-157">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="c035e-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c035e-158">-StorageAccountId</span></span>
<span data-ttu-id="c035e-159">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="c035e-160">-Címke</span><span class="sxs-lookup"><span data-stu-id="c035e-160">-Tag</span></span>
<span data-ttu-id="c035e-161">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="c035e-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c035e-162">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="c035e-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c035e-163">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="c035e-163">-UploadSizeInBytes</span></span>
<span data-ttu-id="c035e-164">A feltöltés CreateOption a VHD-láblécet tartalmazó feltöltés tartalmának méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-164">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="c035e-165">Ennek az értéknek a 20972032-as (20 MiB + 512 bájtnál a VHD-lábléchez) és az 35183298347520 bájt (32 TiB + 512 bájt a VHD-láblécben) között kell lennie.</span><span class="sxs-lookup"><span data-stu-id="c035e-165">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="c035e-166">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="c035e-166">-Zone</span></span>
<span data-ttu-id="c035e-167">A lemez logikai zóna-listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="c035e-167">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="c035e-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c035e-168">-Confirm</span></span>
<span data-ttu-id="c035e-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c035e-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c035e-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c035e-170">-WhatIf</span></span>
<span data-ttu-id="c035e-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c035e-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c035e-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c035e-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c035e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c035e-173">CommonParameters</span></span>
<span data-ttu-id="c035e-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c035e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c035e-175">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c035e-175">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c035e-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c035e-176">INPUTS</span></span>

### <span data-ttu-id="c035e-177">System. String</span><span class="sxs-lookup"><span data-stu-id="c035e-177">System.String</span></span>

### <span data-ttu-id="c035e-178">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 23.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c035e-178">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c035e-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c035e-179">System.Int32</span></span>

### <span data-ttu-id="c035e-180">System. string []</span><span class="sxs-lookup"><span data-stu-id="c035e-180">System.String[]</span></span>

### <span data-ttu-id="c035e-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c035e-181">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c035e-182">Microsoft. Azure. Management. kiszámítás. models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="c035e-182">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="c035e-183">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c035e-183">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c035e-184">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="c035e-184">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="c035e-185">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="c035e-185">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="c035e-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c035e-186">OUTPUTS</span></span>

### <span data-ttu-id="c035e-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="c035e-187">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="c035e-188">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c035e-188">NOTES</span></span>

## <span data-ttu-id="c035e-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c035e-189">RELATED LINKS</span></span>
