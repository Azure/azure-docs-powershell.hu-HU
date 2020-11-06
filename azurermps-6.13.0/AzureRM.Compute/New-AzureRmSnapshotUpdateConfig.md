---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotUpdateConfig.md
ms.openlocfilehash: 31c3ca819619f791f706fe93ce4977508fb28d27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499688"
---
# <span data-ttu-id="da940-101">New-AzureRmSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="da940-101">New-AzureRmSnapshotUpdateConfig</span></span>

## <span data-ttu-id="da940-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da940-102">SYNOPSIS</span></span>
<span data-ttu-id="da940-103">Konfigurálható Snapshot Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da940-103">Creates a configurable snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da940-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da940-104">SYNTAX</span></span>

```
New-AzureRmSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da940-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="da940-105">DESCRIPTION</span></span>
<span data-ttu-id="da940-106">A **New-AzureRmSnapshotUpdateConfig** parancsmag egy konfigurálható Snapshot Update-objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="da940-106">The **New-AzureRmSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="da940-107">Példák</span><span class="sxs-lookup"><span data-stu-id="da940-107">EXAMPLES</span></span>

### <span data-ttu-id="da940-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da940-108">Example 1</span></span>
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

<span data-ttu-id="da940-109">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="da940-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="da940-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="da940-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="da940-111">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="da940-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="da940-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="da940-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="da940-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="da940-113">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="da940-114">Ez a parancs frissíti a meglévő, "Snapshot01" nevű pillanatképet a "ResourceGroup01" és a 10 GB méretű merevlemez között.</span><span class="sxs-lookup"><span data-stu-id="da940-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="da940-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da940-115">PARAMETERS</span></span>

### <span data-ttu-id="da940-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da940-116">-DefaultProfile</span></span>
<span data-ttu-id="da940-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da940-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da940-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="da940-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="da940-119">A lemez titkosítási kulcs objektumát adja meg egy pillanatképen.</span><span class="sxs-lookup"><span data-stu-id="da940-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="da940-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="da940-120">-DiskSizeGB</span></span>
<span data-ttu-id="da940-121">A lemezmeghajtó méretének meghatározása GB-ban.</span><span class="sxs-lookup"><span data-stu-id="da940-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="da940-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="da940-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="da940-123">Titkosítási beállítások engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="da940-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="da940-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="da940-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="da940-125">Egy pillanatkép kulcs titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="da940-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="da940-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="da940-126">-OsType</span></span>
<span data-ttu-id="da940-127">Az operációs rendszer típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="da940-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="da940-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="da940-128">-SkuName</span></span>
<span data-ttu-id="da940-129">Megadja a tárolási fiók SKU-nevét.</span><span class="sxs-lookup"><span data-stu-id="da940-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="da940-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="da940-130">-Tag</span></span>
<span data-ttu-id="da940-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="da940-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="da940-132">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="da940-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da940-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da940-133">-Confirm</span></span>
<span data-ttu-id="da940-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da940-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da940-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da940-135">-WhatIf</span></span>
<span data-ttu-id="da940-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da940-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da940-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da940-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da940-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da940-138">CommonParameters</span></span>
<span data-ttu-id="da940-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da940-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da940-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da940-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da940-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da940-141">INPUTS</span></span>

### <span data-ttu-id="da940-142">System. String</span><span class="sxs-lookup"><span data-stu-id="da940-142">System.String</span></span>

### <span data-ttu-id="da940-143">System. nulla ' 1 [[Microsoft. Azure. Management. kiszámítás. models. OperatingSystemTypes, Microsoft. Azure. Management. kiszámítás, Version = 21.0.0.0, Culture = semleges, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="da940-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="da940-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="da940-144">System.Int32</span></span>

### <span data-ttu-id="da940-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="da940-145">System.Collections.Hashtable</span></span>

### <span data-ttu-id="da940-146">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="da940-146">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="da940-147">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="da940-147">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="da940-148">Microsoft. Azure. Management. kiszámítás. models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="da940-148">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="da940-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da940-149">OUTPUTS</span></span>

### <span data-ttu-id="da940-150">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="da940-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="da940-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da940-151">NOTES</span></span>

## <span data-ttu-id="da940-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da940-152">RELATED LINKS</span></span>
