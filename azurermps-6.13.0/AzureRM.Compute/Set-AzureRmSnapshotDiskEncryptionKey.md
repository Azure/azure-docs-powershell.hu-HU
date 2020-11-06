---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmSnapshotDiskEncryptionKey.md
ms.openlocfilehash: d5bbb921cf913490ba21bcadda4fda8ce6f97a03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491984"
---
# <span data-ttu-id="0ac3e-101">Set-AzureRmSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0ac3e-101">Set-AzureRmSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="0ac3e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ac3e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ac3e-103">A lemezvezérlő-titkosítási kulcs tulajdonságainak megadása egy pillanatkép-objektumon.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-103">Sets the disk encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ac3e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ac3e-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ac3e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ac3e-105">DESCRIPTION</span></span>
<span data-ttu-id="0ac3e-106">A **set-AzureRmSnapshotDiskEncryptionKey** parancsmag a titkosító kulcs tulajdonságait állítja be egy pillanatkép-objektumon.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-106">The **Set-AzureRmSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="0ac3e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ac3e-107">EXAMPLES</span></span>

### <span data-ttu-id="0ac3e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0ac3e-108">Example 1</span></span>
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

<span data-ttu-id="0ac3e-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0ac3e-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0ac3e-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="0ac3e-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0ac3e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ac3e-113">PARAMETERS</span></span>

### <span data-ttu-id="0ac3e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ac3e-114">-DefaultProfile</span></span>
<span data-ttu-id="0ac3e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ac3e-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="0ac3e-116">-SecretUrl</span></span>
<span data-ttu-id="0ac3e-117">A titkos URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="0ac3e-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="0ac3e-118">-Snapshot</span></span>
<span data-ttu-id="0ac3e-119">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="0ac3e-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0ac3e-120">-SourceVaultId</span></span>
<span data-ttu-id="0ac3e-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="0ac3e-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0ac3e-122">-Confirm</span></span>
<span data-ttu-id="0ac3e-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ac3e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ac3e-124">-WhatIf</span></span>
<span data-ttu-id="0ac3e-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ac3e-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ac3e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ac3e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ac3e-127">CommonParameters</span></span>
<span data-ttu-id="0ac3e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ac3e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ac3e-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ac3e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ac3e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ac3e-130">INPUTS</span></span>

### <span data-ttu-id="0ac3e-131">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0ac3e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="0ac3e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0ac3e-132">System.String</span></span>

## <span data-ttu-id="0ac3e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ac3e-133">OUTPUTS</span></span>

### <span data-ttu-id="0ac3e-134">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0ac3e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0ac3e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ac3e-135">NOTES</span></span>

## <span data-ttu-id="0ac3e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ac3e-136">RELATED LINKS</span></span>
