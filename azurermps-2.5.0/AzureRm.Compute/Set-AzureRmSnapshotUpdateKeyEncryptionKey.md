---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotupdatekeyencryptionkey
schema: 2.0.0
ms.openlocfilehash: 10dde05cb4be4672f81c656ffcb4f2ae732f0916
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848494"
---
# <span data-ttu-id="1a980-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1a980-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="1a980-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a980-102">SYNOPSIS</span></span>
<span data-ttu-id="1a980-103">A kulcs titkosítási kulcs tulajdonságait állítja be egy Snapshot Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="1a980-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a980-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a980-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a980-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a980-105">DESCRIPTION</span></span>
<span data-ttu-id="1a980-106">A **set-AzureRmSnapshotUpdateKeyEncryptionKey** parancsmag a fontos titkosítási kulcs tulajdonságait állítja be a Snapshot Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="1a980-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="1a980-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1a980-107">EXAMPLES</span></span>

### <span data-ttu-id="1a980-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1a980-108">Example 1</span></span>
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

<span data-ttu-id="1a980-109">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="1a980-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="1a980-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="1a980-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="1a980-111">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="1a980-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="1a980-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="1a980-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1a980-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a980-113">PARAMETERS</span></span>

### <span data-ttu-id="1a980-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a980-114">-DefaultProfile</span></span>
<span data-ttu-id="1a980-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a980-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a980-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="1a980-116">-KeyUrl</span></span>
<span data-ttu-id="1a980-117">Specifes a legfontosabb URL-címet.</span><span class="sxs-lookup"><span data-stu-id="1a980-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="1a980-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="1a980-118">-SnapshotUpdate</span></span>
<span data-ttu-id="1a980-119">Egy helyi Snapshot Update-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1a980-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a980-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1a980-120">-SourceVaultId</span></span>
<span data-ttu-id="1a980-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a980-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="1a980-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1a980-122">-Confirm</span></span>
<span data-ttu-id="1a980-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1a980-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a980-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a980-124">-WhatIf</span></span>
<span data-ttu-id="1a980-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1a980-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a980-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a980-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a980-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a980-127">CommonParameters</span></span>
<span data-ttu-id="1a980-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a980-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a980-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a980-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a980-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a980-130">INPUTS</span></span>

### <span data-ttu-id="1a980-131">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="1a980-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="1a980-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a980-132">System.String</span></span>

## <span data-ttu-id="1a980-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a980-133">OUTPUTS</span></span>

### <span data-ttu-id="1a980-134">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="1a980-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="1a980-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a980-135">NOTES</span></span>

## <span data-ttu-id="1a980-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a980-136">RELATED LINKS</span></span>
