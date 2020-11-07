---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673003"
---
# <span data-ttu-id="e0db8-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="e0db8-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="e0db8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0db8-102">SYNOPSIS</span></span>
<span data-ttu-id="e0db8-103">Konfigurálható lemezkezelő-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e0db8-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0db8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0db8-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0db8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0db8-105">DESCRIPTION</span></span>
<span data-ttu-id="e0db8-106">A **New-AzureRmDiskConfig** parancsmag létrehoz egy konfigurálható Disk-objektumot.</span><span class="sxs-lookup"><span data-stu-id="e0db8-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="e0db8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e0db8-107">EXAMPLES</span></span>

### <span data-ttu-id="e0db8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e0db8-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e0db8-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="e0db8-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="e0db8-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="e0db8-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="e0db8-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0db8-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="e0db8-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="e0db8-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e0db8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0db8-113">PARAMETERS</span></span>

### <span data-ttu-id="e0db8-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e0db8-114">-CreateOption</span></span>
<span data-ttu-id="e0db8-115">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="e0db8-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="e0db8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0db8-116">-DefaultProfile</span></span>
<span data-ttu-id="e0db8-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e0db8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0db8-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e0db8-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="e0db8-119">A lemez titkosítási kulcs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0db8-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="e0db8-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="e0db8-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="e0db8-121">A lemezre engedélyezett IOPS száma; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="e0db8-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e0db8-122">Egy művelet átadható a 4k és a 256k között.</span><span class="sxs-lookup"><span data-stu-id="e0db8-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="e0db8-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="e0db8-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="e0db8-124">A lemezre engedélyezett sávszélesség; csak a UltraSSD-lemezek állíthatók be.</span><span class="sxs-lookup"><span data-stu-id="e0db8-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="e0db8-125">MBps: a 10 MB/s sebességű bájtok száma itt az ISO-jelölést használja, a 10-es hatáskörökkel.</span><span class="sxs-lookup"><span data-stu-id="e0db8-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="e0db8-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e0db8-126">-DiskSizeGB</span></span>
<span data-ttu-id="e0db8-127">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="e0db8-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e0db8-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e0db8-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e0db8-129">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="e0db8-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e0db8-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="e0db8-130">-ImageReference</span></span>
<span data-ttu-id="e0db8-131">A kép hivatkozását adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="e0db8-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="e0db8-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e0db8-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="e0db8-133">A kulcs titkosítási kulcsát adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="e0db8-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="e0db8-134">-Hely</span><span class="sxs-lookup"><span data-stu-id="e0db8-134">-Location</span></span>
<span data-ttu-id="e0db8-135">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="e0db8-135">Specifies a location.</span></span>

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

### <span data-ttu-id="e0db8-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="e0db8-136">-OsType</span></span>
<span data-ttu-id="e0db8-137">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0db8-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e0db8-138">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e0db8-138">-SkuName</span></span>
<span data-ttu-id="e0db8-139">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="e0db8-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="e0db8-140">A rendelkezésre álló értékek az Standard_LRS, a Premium_LRS, a StandardSSD_LRS és a UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="e0db8-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="e0db8-141">A UltraSSD_LRS csak a CreateOption paraméter üres értékével használható.</span><span class="sxs-lookup"><span data-stu-id="e0db8-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="e0db8-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e0db8-142">-SourceResourceId</span></span>
<span data-ttu-id="e0db8-143">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0db8-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="e0db8-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="e0db8-144">-SourceUri</span></span>
<span data-ttu-id="e0db8-145">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0db8-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="e0db8-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e0db8-146">-StorageAccountId</span></span>
<span data-ttu-id="e0db8-147">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0db8-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="e0db8-148">-Címke</span><span class="sxs-lookup"><span data-stu-id="e0db8-148">-Tag</span></span>
<span data-ttu-id="e0db8-149">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="e0db8-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e0db8-150">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="e0db8-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e0db8-151">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="e0db8-151">-Zone</span></span>
<span data-ttu-id="e0db8-152">A lemez logikai zóna-listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0db8-152">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="e0db8-153">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0db8-153">-Confirm</span></span>
<span data-ttu-id="e0db8-154">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0db8-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0db8-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0db8-155">-WhatIf</span></span>
<span data-ttu-id="e0db8-156">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0db8-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0db8-157">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0db8-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0db8-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0db8-158">CommonParameters</span></span>
<span data-ttu-id="e0db8-159">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0db8-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0db8-160">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0db8-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0db8-161">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0db8-161">INPUTS</span></span>

### <span data-ttu-id="e0db8-162">System. String</span><span class="sxs-lookup"><span data-stu-id="e0db8-162">System.String</span></span>

### <span data-ttu-id="e0db8-163">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 21.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e0db8-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e0db8-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e0db8-164">System.Int32</span></span>

### <span data-ttu-id="e0db8-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="e0db8-165">System.String[]</span></span>

### <span data-ttu-id="e0db8-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e0db8-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e0db8-167">Microsoft. Azure. Management. kiszámítás. models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="e0db8-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="e0db8-168">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e0db8-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e0db8-169">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="e0db8-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="e0db8-170">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="e0db8-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="e0db8-171">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0db8-171">OUTPUTS</span></span>

### <span data-ttu-id="e0db8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="e0db8-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e0db8-173">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0db8-173">NOTES</span></span>

## <span data-ttu-id="e0db8-174">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0db8-174">RELATED LINKS</span></span>
