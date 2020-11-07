---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskupdateconfig
schema: 2.0.0
ms.openlocfilehash: 790d366ced8b9466a906df2d3f1717ad9277ca9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850145"
---
# <span data-ttu-id="ccde7-101">New-AzureRmDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="ccde7-101">New-AzureRmDiskUpdateConfig</span></span>

## <span data-ttu-id="ccde7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ccde7-102">SYNOPSIS</span></span>
<span data-ttu-id="ccde7-103">Konfigurálható Disk Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ccde7-103">Creates a configurable disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccde7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ccde7-104">SYNTAX</span></span>

```
New-AzureRmDiskUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccde7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ccde7-105">DESCRIPTION</span></span>
<span data-ttu-id="ccde7-106">A **New-AzureRmDiskUpdateConfig** parancsmag egy konfigurálható Disk Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ccde7-106">The **New-AzureRmDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="ccde7-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ccde7-107">EXAMPLES</span></span>

### <span data-ttu-id="ccde7-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ccde7-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="ccde7-109">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="ccde7-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="ccde7-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="ccde7-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ccde7-111">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccde7-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ccde7-112">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="ccde7-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ccde7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ccde7-113">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="ccde7-114">Ez a parancs frissíti a "Disk01" nevű, a "ResourceGroup01" nevű, 10 GB-nyi méretű kötetet használó meglévő lemezt.</span><span class="sxs-lookup"><span data-stu-id="ccde7-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="ccde7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ccde7-115">PARAMETERS</span></span>

### <span data-ttu-id="ccde7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccde7-116">-DefaultProfile</span></span>
<span data-ttu-id="ccde7-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ccde7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccde7-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ccde7-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="ccde7-119">A lemez titkosítási kulcs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccde7-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="ccde7-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ccde7-120">-DiskSizeGB</span></span>
<span data-ttu-id="ccde7-121">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="ccde7-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ccde7-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ccde7-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ccde7-123">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="ccde7-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ccde7-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ccde7-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="ccde7-125">A kulcs titkosítási kulcsát adja meg a lemezen.</span><span class="sxs-lookup"><span data-stu-id="ccde7-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="ccde7-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="ccde7-126">-OsType</span></span>
<span data-ttu-id="ccde7-127">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ccde7-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ccde7-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ccde7-128">-SkuName</span></span>
<span data-ttu-id="ccde7-129">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="ccde7-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="ccde7-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="ccde7-130">-Tag</span></span>
<span data-ttu-id="ccde7-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="ccde7-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ccde7-132">Példa:</span><span class="sxs-lookup"><span data-stu-id="ccde7-132">For example:</span></span>

<span data-ttu-id="ccde7-133">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="ccde7-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ccde7-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ccde7-134">-Confirm</span></span>
<span data-ttu-id="ccde7-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ccde7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccde7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccde7-136">-WhatIf</span></span>
<span data-ttu-id="ccde7-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ccde7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccde7-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ccde7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccde7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccde7-139">CommonParameters</span></span>
<span data-ttu-id="ccde7-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ccde7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccde7-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccde7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccde7-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccde7-142">INPUTS</span></span>

### <span data-ttu-id="ccde7-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="ccde7-143">None</span></span>
<span data-ttu-id="ccde7-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ccde7-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ccde7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ccde7-145">OUTPUTS</span></span>

### <span data-ttu-id="ccde7-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ccde7-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="ccde7-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ccde7-147">NOTES</span></span>

## <span data-ttu-id="ccde7-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ccde7-148">RELATED LINKS</span></span>

