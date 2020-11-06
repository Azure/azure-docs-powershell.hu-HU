---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotKeyEncryptionKey.md
ms.openlocfilehash: 9c6debcae0aa83dd08374c7e390e3a42c4e5233a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492361"
---
# <span data-ttu-id="6d73a-101">Set-AzureRmSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6d73a-101">Set-AzureRmSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="6d73a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6d73a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d73a-103">A kulcs titkosítási kulcs tulajdonságait állítja be egy pillanatkép-objektumon.</span><span class="sxs-lookup"><span data-stu-id="6d73a-103">Sets the key encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d73a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6d73a-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotKeyEncryptionKey [-Snapshot] <Snapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d73a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6d73a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d73a-106">A **set-AzureRmSnapshotKeyEncryptionKey** parancsmag a fontos titkosítási kulcs tulajdonságait állítja be egy pillanatkép-objektumon.</span><span class="sxs-lookup"><span data-stu-id="6d73a-106">The **Set-AzureRmSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="6d73a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6d73a-107">EXAMPLES</span></span>

### <span data-ttu-id="6d73a-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6d73a-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="6d73a-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="6d73a-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="6d73a-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="6d73a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6d73a-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="6d73a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="6d73a-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="6d73a-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6d73a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6d73a-113">PARAMETERS</span></span>

### <span data-ttu-id="6d73a-114">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="6d73a-114">-KeyUrl</span></span>
<span data-ttu-id="6d73a-115">Specifes a legfontosabb URL-címet.</span><span class="sxs-lookup"><span data-stu-id="6d73a-115">Specifes the key Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d73a-116">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="6d73a-116">-Snapshot</span></span>
<span data-ttu-id="6d73a-117">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="6d73a-117">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d73a-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6d73a-118">-SourceVaultId</span></span>
<span data-ttu-id="6d73a-119">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6d73a-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d73a-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6d73a-120">-Confirm</span></span>
<span data-ttu-id="6d73a-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6d73a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d73a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d73a-122">-WhatIf</span></span>
<span data-ttu-id="6d73a-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6d73a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d73a-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d73a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d73a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d73a-125">CommonParameters</span></span>
<span data-ttu-id="6d73a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6d73a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d73a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d73a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d73a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d73a-128">INPUTS</span></span>

### <span data-ttu-id="6d73a-129">Microsoft. Azure. Management. számítás. models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="6d73a-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="6d73a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6d73a-130">System.String</span></span>

## <span data-ttu-id="6d73a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d73a-131">OUTPUTS</span></span>

### <span data-ttu-id="6d73a-132">Microsoft. Azure. Management. számítás. models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="6d73a-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="6d73a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6d73a-133">NOTES</span></span>

## <span data-ttu-id="6d73a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d73a-134">RELATED LINKS</span></span>

