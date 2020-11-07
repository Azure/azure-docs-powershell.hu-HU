---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: 8b1fa88954c95c8f49af4767e353bba5a42e3a92
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844262"
---
# <span data-ttu-id="29465-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="29465-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="29465-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="29465-102">SYNOPSIS</span></span>
<span data-ttu-id="29465-103">A kulcs titkosítási kulcs tulajdonságait állítja be egy Snapshot Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="29465-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="29465-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="29465-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29465-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="29465-105">DESCRIPTION</span></span>
<span data-ttu-id="29465-106">A **set-AzSnapshotUpdateKeyEncryptionKey** parancsmag a fontos titkosítási kulcs tulajdonságait állítja be a Snapshot Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="29465-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="29465-107">Példák</span><span class="sxs-lookup"><span data-stu-id="29465-107">EXAMPLES</span></span>

### <span data-ttu-id="29465-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="29465-108">Example 1</span></span>
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

<span data-ttu-id="29465-109">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="29465-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="29465-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="29465-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="29465-111">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="29465-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="29465-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="29465-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="29465-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="29465-113">PARAMETERS</span></span>

### <span data-ttu-id="29465-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29465-114">-DefaultProfile</span></span>
<span data-ttu-id="29465-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="29465-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29465-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="29465-116">-KeyUrl</span></span>
<span data-ttu-id="29465-117">Specifes a legfontosabb URL-címet.</span><span class="sxs-lookup"><span data-stu-id="29465-117">Specifes the key Url.</span></span>

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

### <span data-ttu-id="29465-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="29465-118">-SnapshotUpdate</span></span>
<span data-ttu-id="29465-119">Egy helyi Snapshot Update-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="29465-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="29465-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="29465-120">-SourceVaultId</span></span>
<span data-ttu-id="29465-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="29465-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="29465-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="29465-122">-Confirm</span></span>
<span data-ttu-id="29465-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="29465-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29465-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29465-124">-WhatIf</span></span>
<span data-ttu-id="29465-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="29465-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29465-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="29465-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29465-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29465-127">CommonParameters</span></span>
<span data-ttu-id="29465-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="29465-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29465-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29465-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29465-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="29465-130">INPUTS</span></span>

### <span data-ttu-id="29465-131">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="29465-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="29465-132">System. String</span><span class="sxs-lookup"><span data-stu-id="29465-132">System.String</span></span>

## <span data-ttu-id="29465-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="29465-133">OUTPUTS</span></span>

### <span data-ttu-id="29465-134">Microsoft. Azure. Management. kiszámítás. models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="29465-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="29465-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="29465-135">NOTES</span></span>

## <span data-ttu-id="29465-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="29465-136">RELATED LINKS</span></span>

