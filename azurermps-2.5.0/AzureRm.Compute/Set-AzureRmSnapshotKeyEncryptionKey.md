---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotkeyencryptionkey
schema: 2.0.0
ms.openlocfilehash: f1ca99aacc8e2c737ed8ddbbe9fa899afe78c12a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848502"
---
# <span data-ttu-id="0bcf4-101">Set-AzureRmSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0bcf4-101">Set-AzureRmSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="0bcf4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0bcf4-102">SYNOPSIS</span></span>
<span data-ttu-id="0bcf4-103">A kulcs titkosítási kulcs tulajdonságait állítja be egy pillanatkép-objektumon.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-103">Sets the key encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bcf4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0bcf4-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bcf4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0bcf4-105">DESCRIPTION</span></span>
<span data-ttu-id="0bcf4-106">A **set-AzureRmSnapshotKeyEncryptionKey** parancsmag a fontos titkosítási kulcs tulajdonságait állítja be egy pillanatkép-objektumon.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-106">The **Set-AzureRmSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="0bcf4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0bcf4-107">EXAMPLES</span></span>

### <span data-ttu-id="0bcf4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0bcf4-108">Example 1</span></span>
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

<span data-ttu-id="0bcf4-109">Az első parancs létrehoz egy helyi üres pillanatkép-objektumot, az 5GB méretével Standard_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0bcf4-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0bcf4-111">A második és a harmadik parancs beállítja a lemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="0bcf4-112">Az utolsó parancs átveszi a pillanatkép-objektumot, és egy "Snapshot01" nevű pillanatképet hoz létre a "ResourceGroup01" erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0bcf4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0bcf4-113">PARAMETERS</span></span>

### <span data-ttu-id="0bcf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bcf4-114">-DefaultProfile</span></span>
<span data-ttu-id="0bcf4-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bcf4-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="0bcf4-116">-KeyUrl</span></span>
<span data-ttu-id="0bcf4-117">Specifes a legfontosabb URL-címet.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="0bcf4-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="0bcf4-118">-Snapshot</span></span>
<span data-ttu-id="0bcf4-119">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bcf4-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0bcf4-120">-SourceVaultId</span></span>
<span data-ttu-id="0bcf4-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="0bcf4-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0bcf4-122">-Confirm</span></span>
<span data-ttu-id="0bcf4-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bcf4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bcf4-124">-WhatIf</span></span>
<span data-ttu-id="0bcf4-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bcf4-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0bcf4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bcf4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bcf4-127">CommonParameters</span></span>
<span data-ttu-id="0bcf4-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0bcf4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bcf4-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bcf4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bcf4-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bcf4-130">INPUTS</span></span>

### <span data-ttu-id="0bcf4-131">Microsoft. Azure. Management. számítás. models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="0bcf4-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="0bcf4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0bcf4-132">System.String</span></span>

## <span data-ttu-id="0bcf4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bcf4-133">OUTPUTS</span></span>

### <span data-ttu-id="0bcf4-134">Microsoft. Azure. Management. számítás. models. Snapshot</span><span class="sxs-lookup"><span data-stu-id="0bcf4-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="0bcf4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0bcf4-135">NOTES</span></span>

## <span data-ttu-id="0bcf4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bcf4-136">RELATED LINKS</span></span>

