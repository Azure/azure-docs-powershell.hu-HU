---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 851687bdc00b25bd283433fbc00254380a8ef3a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844505"
---
# <span data-ttu-id="aae40-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="aae40-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="aae40-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aae40-102">SYNOPSIS</span></span>
<span data-ttu-id="aae40-103">Konfigurálható lemezkezelő-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aae40-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="aae40-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aae40-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aae40-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aae40-105">DESCRIPTION</span></span>
<span data-ttu-id="aae40-106">A **New-AzDiskConfig** parancsmag létrehoz egy konfigurálható Disk-objektumot.</span><span class="sxs-lookup"><span data-stu-id="aae40-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="aae40-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aae40-107">EXAMPLES</span></span>

### <span data-ttu-id="aae40-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="aae40-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="aae40-109">Az első parancs létrehoz egy helyi üres lemez-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusa.</span><span class="sxs-lookup"><span data-stu-id="aae40-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="aae40-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="aae40-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="aae40-111">A második és a harmadik parancs a Disk-objektum titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae40-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="aae40-112">Az utolsó parancs a Disk objektumot viszi, és egy "Disk01" nevű lemezt hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="aae40-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="aae40-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aae40-113">PARAMETERS</span></span>

### <span data-ttu-id="aae40-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="aae40-114">-CreateOption</span></span>
<span data-ttu-id="aae40-115">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="aae40-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae40-116">-DefaultProfile</span></span>
<span data-ttu-id="aae40-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aae40-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aae40-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aae40-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="aae40-119">A lemez titkosítási kulcs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae40-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="aae40-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="aae40-120">-DiskSizeGB</span></span>
<span data-ttu-id="aae40-121">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="aae40-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="aae40-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="aae40-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="aae40-123">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="aae40-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="aae40-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="aae40-124">-ImageReference</span></span>
<span data-ttu-id="aae40-125">A kép hivatkozását adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="aae40-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="aae40-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aae40-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="aae40-127">A kulcs titkosítási kulcsát adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="aae40-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="aae40-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="aae40-128">-Location</span></span>
<span data-ttu-id="aae40-129">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="aae40-129">Specifies a location.</span></span>

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

### <span data-ttu-id="aae40-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="aae40-130">-OsType</span></span>
<span data-ttu-id="aae40-131">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae40-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="aae40-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="aae40-132">-SkuName</span></span>
<span data-ttu-id="aae40-133">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="aae40-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae40-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="aae40-134">-SourceResourceId</span></span>
<span data-ttu-id="aae40-135">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae40-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="aae40-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="aae40-136">-SourceUri</span></span>
<span data-ttu-id="aae40-137">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae40-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="aae40-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="aae40-138">-StorageAccountId</span></span>
<span data-ttu-id="aae40-139">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae40-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="aae40-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="aae40-140">-Tag</span></span>
<span data-ttu-id="aae40-141">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="aae40-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aae40-142">Példa:</span><span class="sxs-lookup"><span data-stu-id="aae40-142">For example:</span></span>

<span data-ttu-id="aae40-143">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="aae40-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aae40-144">-Zone (zóna)</span><span class="sxs-lookup"><span data-stu-id="aae40-144">-Zone</span></span>
<span data-ttu-id="aae40-145">A lemez logikai zóna-listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="aae40-145">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aae40-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aae40-146">-Confirm</span></span>
<span data-ttu-id="aae40-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aae40-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aae40-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aae40-148">-WhatIf</span></span>
<span data-ttu-id="aae40-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aae40-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aae40-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aae40-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aae40-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae40-151">CommonParameters</span></span>
<span data-ttu-id="aae40-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aae40-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae40-153">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aae40-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae40-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aae40-154">INPUTS</span></span>

### <span data-ttu-id="aae40-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="aae40-155">None</span></span>
<span data-ttu-id="aae40-156">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="aae40-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aae40-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aae40-157">OUTPUTS</span></span>

### <span data-ttu-id="aae40-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="aae40-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="aae40-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aae40-159">NOTES</span></span>

## <span data-ttu-id="aae40-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aae40-160">RELATED LINKS</span></span>

