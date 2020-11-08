---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: e4ecb281382af308176f47462e086f69c18e6163
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010857"
---
# <span data-ttu-id="54f54-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="54f54-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="54f54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="54f54-102">SYNOPSIS</span></span>
<span data-ttu-id="54f54-103">A lemezvezérlő-titkosítási kulcs tulajdonságainak megadása egy pillanatkép-objektumon.</span><span class="sxs-lookup"><span data-stu-id="54f54-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="54f54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="54f54-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54f54-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="54f54-105">DESCRIPTION</span></span>
<span data-ttu-id="54f54-106">A **set-AzSnapshotDiskEncryptionKey** parancsmag a titkosító kulcs tulajdonságait állítja be egy pillanatkép-objektumon.</span><span class="sxs-lookup"><span data-stu-id="54f54-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="54f54-107">Példák</span><span class="sxs-lookup"><span data-stu-id="54f54-107">EXAMPLES</span></span>

### <span data-ttu-id="54f54-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="54f54-108">Example 1</span></span>
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

<span data-ttu-id="54f54-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="54f54-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="54f54-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="54f54-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="54f54-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="54f54-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="54f54-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="54f54-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="54f54-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="54f54-113">PARAMETERS</span></span>

### <span data-ttu-id="54f54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f54-114">-DefaultProfile</span></span>
<span data-ttu-id="54f54-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="54f54-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54f54-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="54f54-116">-SecretUrl</span></span>
<span data-ttu-id="54f54-117">A titkos URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="54f54-117">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f54-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="54f54-118">-Snapshot</span></span>
<span data-ttu-id="54f54-119">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="54f54-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54f54-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="54f54-120">-SourceVaultId</span></span>
<span data-ttu-id="54f54-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="54f54-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f54-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="54f54-122">-Confirm</span></span>
<span data-ttu-id="54f54-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="54f54-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f54-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54f54-124">-WhatIf</span></span>
<span data-ttu-id="54f54-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="54f54-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54f54-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="54f54-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f54-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f54-127">CommonParameters</span></span>
<span data-ttu-id="54f54-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="54f54-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f54-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="54f54-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f54-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="54f54-130">INPUTS</span></span>

### <span data-ttu-id="54f54-131">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="54f54-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="54f54-132">System. String</span><span class="sxs-lookup"><span data-stu-id="54f54-132">System.String</span></span>

## <span data-ttu-id="54f54-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="54f54-133">OUTPUTS</span></span>

### <span data-ttu-id="54f54-134">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="54f54-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="54f54-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="54f54-135">NOTES</span></span>

## <span data-ttu-id="54f54-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="54f54-136">RELATED LINKS</span></span>
