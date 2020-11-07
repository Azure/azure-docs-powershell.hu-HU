---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 1afd1631e398b5726a8e1002b6739fc7ac9b67a8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844482"
---
# <span data-ttu-id="ee781-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ee781-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="ee781-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee781-102">SYNOPSIS</span></span>
<span data-ttu-id="ee781-103">Konfigurálható pillanatkép-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ee781-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="ee781-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee781-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee781-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee781-105">DESCRIPTION</span></span>
<span data-ttu-id="ee781-106">A **New-AzSnapshotConfig** parancsmag létrehoz egy konfigurálható pillanatkép-objektumot.</span><span class="sxs-lookup"><span data-stu-id="ee781-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="ee781-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee781-107">EXAMPLES</span></span>

### <span data-ttu-id="ee781-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ee781-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="ee781-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="ee781-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="ee781-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="ee781-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ee781-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="ee781-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="ee781-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="ee781-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ee781-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee781-113">PARAMETERS</span></span>

### <span data-ttu-id="ee781-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="ee781-114">-CreateOption</span></span>
<span data-ttu-id="ee781-115">Itt adhatja meg, hogy a parancsmag létrehoz-e egy lemezt a virtuális gépen egy platformról vagy egy felhasználói képből, létrehoz egy üres lemezt, vagy csatol egy meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="ee781-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="ee781-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee781-116">-DefaultProfile</span></span>
<span data-ttu-id="ee781-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee781-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee781-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ee781-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="ee781-119">A lemez titkosítási kulcs objektumát adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="ee781-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="ee781-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ee781-120">-DiskSizeGB</span></span>
<span data-ttu-id="ee781-121">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="ee781-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ee781-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ee781-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ee781-123">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="ee781-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ee781-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="ee781-124">-ImageReference</span></span>
<span data-ttu-id="ee781-125">A kép hivatkozását adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="ee781-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="ee781-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ee781-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="ee781-127">Egy pillanatkép kulcs titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee781-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="ee781-128">-Hely</span><span class="sxs-lookup"><span data-stu-id="ee781-128">-Location</span></span>
<span data-ttu-id="ee781-129">Helyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="ee781-129">Specifies a location.</span></span>

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

### <span data-ttu-id="ee781-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="ee781-130">-OsType</span></span>
<span data-ttu-id="ee781-131">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee781-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ee781-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ee781-132">-SkuName</span></span>
<span data-ttu-id="ee781-133">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="ee781-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="ee781-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ee781-134">-SourceResourceId</span></span>
<span data-ttu-id="ee781-135">A forrás erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee781-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="ee781-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ee781-136">-SourceUri</span></span>
<span data-ttu-id="ee781-137">A forrás URI-azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee781-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="ee781-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ee781-138">-StorageAccountId</span></span>
<span data-ttu-id="ee781-139">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee781-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="ee781-140">-Címke</span><span class="sxs-lookup"><span data-stu-id="ee781-140">-Tag</span></span>
<span data-ttu-id="ee781-141">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="ee781-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ee781-142">Példa:</span><span class="sxs-lookup"><span data-stu-id="ee781-142">For example:</span></span>

<span data-ttu-id="ee781-143">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="ee781-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ee781-144">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee781-144">-Confirm</span></span>
<span data-ttu-id="ee781-145">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee781-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee781-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee781-146">-WhatIf</span></span>
<span data-ttu-id="ee781-147">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee781-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee781-148">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee781-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee781-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee781-149">CommonParameters</span></span>
<span data-ttu-id="ee781-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee781-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee781-151">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee781-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee781-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee781-152">INPUTS</span></span>

### <span data-ttu-id="ee781-153">Nincs</span><span class="sxs-lookup"><span data-stu-id="ee781-153">None</span></span>
<span data-ttu-id="ee781-154">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ee781-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee781-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee781-155">OUTPUTS</span></span>

### <span data-ttu-id="ee781-156">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ee781-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="ee781-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee781-157">NOTES</span></span>

## <span data-ttu-id="ee781-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee781-158">RELATED LINKS</span></span>

