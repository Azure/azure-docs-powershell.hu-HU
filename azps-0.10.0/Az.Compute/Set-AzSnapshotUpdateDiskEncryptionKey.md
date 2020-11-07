---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: c427c63e6d7e954e2ce832b3d6e5fe3bf7c4a851
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844270"
---
# <span data-ttu-id="431fc-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="431fc-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="431fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="431fc-102">SYNOPSIS</span></span>
<span data-ttu-id="431fc-103">A titkosító kulcs tulajdonságait állítja be egy Snapshot Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="431fc-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="431fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="431fc-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="431fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="431fc-105">DESCRIPTION</span></span>
<span data-ttu-id="431fc-106">A **set-AzSnapshotUpdateDiskEncryptionKey** parancsmag a titkosító kulcs tulajdonságait a Snapshot Update objektumban állítja be.</span><span class="sxs-lookup"><span data-stu-id="431fc-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="431fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="431fc-107">EXAMPLES</span></span>

### <span data-ttu-id="431fc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="431fc-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="431fc-109">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="431fc-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="431fc-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="431fc-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="431fc-111">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="431fc-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="431fc-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="431fc-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="431fc-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="431fc-113">PARAMETERS</span></span>

### <span data-ttu-id="431fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="431fc-114">-DefaultProfile</span></span>
<span data-ttu-id="431fc-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="431fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="431fc-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="431fc-116">-SecretUrl</span></span>
<span data-ttu-id="431fc-117">Specifes a titkos URL-címet.</span><span class="sxs-lookup"><span data-stu-id="431fc-117">Specifes the secret Url.</span></span>

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

### <span data-ttu-id="431fc-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="431fc-118">-SnapshotUpdate</span></span>
<span data-ttu-id="431fc-119">Egy helyi Snapshot Update-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="431fc-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="431fc-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="431fc-120">-SourceVaultId</span></span>
<span data-ttu-id="431fc-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="431fc-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="431fc-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="431fc-122">-Confirm</span></span>
<span data-ttu-id="431fc-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="431fc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="431fc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="431fc-124">-WhatIf</span></span>
<span data-ttu-id="431fc-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="431fc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="431fc-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="431fc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="431fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="431fc-127">CommonParameters</span></span>
<span data-ttu-id="431fc-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="431fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="431fc-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="431fc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="431fc-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="431fc-130">INPUTS</span></span>

### <span data-ttu-id="431fc-131">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="431fc-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="431fc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="431fc-132">System.String</span></span>

## <span data-ttu-id="431fc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="431fc-133">OUTPUTS</span></span>

### <span data-ttu-id="431fc-134">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="431fc-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="431fc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="431fc-135">NOTES</span></span>

## <span data-ttu-id="431fc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="431fc-136">RELATED LINKS</span></span>

