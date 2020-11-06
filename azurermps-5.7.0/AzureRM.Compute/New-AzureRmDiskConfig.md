---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: b2c922a1dcce683636d61b68c66ab8cfb82535c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495451"
---
# <span data-ttu-id="7adba-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="7adba-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="7adba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7adba-102">SYNOPSIS</span></span>
<span data-ttu-id="7adba-103">Konfigurálható lemezkezelő-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7adba-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7adba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7adba-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7adba-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7adba-105">DESCRIPTION</span></span>
<span data-ttu-id="7adba-106">A **New-AzureRmDiskConfig** parancsmag létrehoz egy konfigurálható Disk-objektumot.</span><span class="sxs-lookup"><span data-stu-id="7adba-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="7adba-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7adba-107">EXAMPLES</span></span>

### <span data-ttu-id="7adba-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7adba-108">Example 1</span></span>
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

<span data-ttu-id="7adba-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="7adba-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="7adba-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="7adba-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="7adba-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7adba-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="7adba-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="7adba-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7adba-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7adba-113">PARAMETERS</span></span>

### <span data-ttu-id="7adba-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="7adba-114">-CreateOption</span></span>
<span data-ttu-id="7adba-115">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="7adba-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7adba-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="7adba-117">A lemez titkosítási kulcs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7adba-117">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7adba-118">-DiskSizeGB</span></span>
<span data-ttu-id="7adba-119">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="7adba-119">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="7adba-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="7adba-121">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="7adba-121">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="7adba-122">-ImageReference</span></span>
<span data-ttu-id="7adba-123">A kép hivatkozását adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="7adba-123">Specifies the image reference on a disk.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7adba-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="7adba-125">A kulcs titkosítási kulcsát adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="7adba-125">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-126">-Hely</span><span class="sxs-lookup"><span data-stu-id="7adba-126">-Location</span></span>
<span data-ttu-id="7adba-127">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="7adba-127">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="7adba-128">-OsType</span></span>
<span data-ttu-id="7adba-129">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7adba-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7adba-130">-SkuName</span></span>
<span data-ttu-id="7adba-131">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="7adba-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7adba-132">-SourceResourceId</span></span>
<span data-ttu-id="7adba-133">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7adba-133">Specifies the  source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="7adba-134">-SourceUri</span></span>
<span data-ttu-id="7adba-135">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7adba-135">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7adba-136">-StorageAccountId</span></span>
<span data-ttu-id="7adba-137">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7adba-137">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="7adba-138">-Tag</span></span>
<span data-ttu-id="7adba-139">Itt adhatja meg, hogy az erőforrások és az erőforráscsoportok a name-Value pairek halmazával legyenek címkézve.</span><span class="sxs-lookup"><span data-stu-id="7adba-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7adba-140">-Confirm</span></span>
<span data-ttu-id="7adba-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7adba-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7adba-142">-WhatIf</span></span>
<span data-ttu-id="7adba-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7adba-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7adba-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7adba-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7adba-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adba-145">CommonParameters</span></span>
<span data-ttu-id="7adba-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7adba-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adba-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7adba-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adba-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7adba-148">INPUTS</span></span>

### <span data-ttu-id="7adba-149">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. StorageAccountTypes, Microsoft. Azure. Management. kiszámítás, Version = 14.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7adba-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="7adba-150">System. null `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] System. String System. Collections. Hashtable System. null `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. számítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="7adba-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="7adba-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7adba-151">OUTPUTS</span></span>

### <span data-ttu-id="7adba-152">Microsoft. Azure. Management. számítás. modellek. Disk</span><span class="sxs-lookup"><span data-stu-id="7adba-152">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="7adba-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7adba-153">NOTES</span></span>

## <span data-ttu-id="7adba-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7adba-154">RELATED LINKS</span></span>

