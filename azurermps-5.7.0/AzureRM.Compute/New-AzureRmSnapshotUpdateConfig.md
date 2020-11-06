---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 97bfd93babc75b09f87e53f62c60cd4fb08ea599
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497712"
---
# <span data-ttu-id="e216e-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="e216e-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="e216e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e216e-102">SYNOPSIS</span></span>
<span data-ttu-id="e216e-103">Konfigurálható Snapshot Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e216e-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e216e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e216e-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e216e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e216e-105">DESCRIPTION</span></span>
<span data-ttu-id="e216e-106">A **New-AzureRmSnapshotUpdateConfig** parancsmag egy konfigurálható Snapshot Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e216e-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="e216e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e216e-107">EXAMPLES</span></span>

### <span data-ttu-id="e216e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e216e-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="e216e-109">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="e216e-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e216e-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="e216e-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e216e-111">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="e216e-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="e216e-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="e216e-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e216e-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="e216e-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="e216e-114">Ez a parancs frissíti a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemez között.</span><span class="sxs-lookup"><span data-stu-id="e216e-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="e216e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e216e-115">PARAMETERS</span></span>

### <span data-ttu-id="e216e-116">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="e216e-116">-CreateOption</span></span>
<span data-ttu-id="e216e-117">Itt adhatja meg, hogy a parancsmag létrehoz-e egy pillanatképet a virtuális gépen egy platformról vagy egy felhasználói képről, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="e216e-117">Specifies whether this cmdlet creates a snapshot in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="e216e-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e216e-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="e216e-119">A lemez titkosítási kulcs objektumát adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="e216e-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="e216e-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="e216e-120">-DiskSizeGB</span></span>
<span data-ttu-id="e216e-121">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="e216e-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="e216e-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="e216e-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="e216e-123">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="e216e-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="e216e-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="e216e-124">-ImageReference</span></span>
<span data-ttu-id="e216e-125">A kép hivatkozását adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="e216e-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="e216e-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e216e-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="e216e-127">Egy pillanatkép kulcs titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e216e-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="e216e-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="e216e-128">-OsType</span></span>
<span data-ttu-id="e216e-129">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e216e-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="e216e-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e216e-130">-SkuName</span></span>
<span data-ttu-id="e216e-131">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="e216e-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="e216e-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e216e-132">-SourceResourceId</span></span>
<span data-ttu-id="e216e-133">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e216e-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="e216e-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="e216e-134">-SourceUri</span></span>
<span data-ttu-id="e216e-135">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e216e-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="e216e-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e216e-136">-StorageAccountId</span></span>
<span data-ttu-id="e216e-137">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e216e-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="e216e-138">-Címke</span><span class="sxs-lookup"><span data-stu-id="e216e-138">-Tag</span></span>
<span data-ttu-id="e216e-139">Itt adhatja meg, hogy az erőforrások és az erőforráscsoportok a name-Value pairek halmazával legyenek címkézve.</span><span class="sxs-lookup"><span data-stu-id="e216e-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e216e-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e216e-140">-Confirm</span></span>
<span data-ttu-id="e216e-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e216e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e216e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e216e-142">-WhatIf</span></span>
<span data-ttu-id="e216e-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e216e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e216e-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e216e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e216e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e216e-145">CommonParameters</span></span>
<span data-ttu-id="e216e-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e216e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e216e-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e216e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e216e-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e216e-148">INPUTS</span></span>

### <span data-ttu-id="e216e-149">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. StorageAccountTypes, Microsoft. Azure. Management. kiszámítás, Version = 14.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e216e-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="e216e-150">System. null `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable System. null `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. számítás. models. KeyVaultAndSecretReference. KeyVaultAndKeyReference. számítás</span><span class="sxs-lookup"><span data-stu-id="e216e-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.String
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="e216e-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e216e-151">OUTPUTS</span></span>

### <span data-ttu-id="e216e-152">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="e216e-152">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="e216e-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e216e-153">NOTES</span></span>

## <span data-ttu-id="e216e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e216e-154">RELATED LINKS</span></span>

