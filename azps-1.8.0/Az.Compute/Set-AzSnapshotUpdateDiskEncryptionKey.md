---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: ce61825c4521d9c257675a1f151b97dbab7fb48b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836677"
---
# <span data-ttu-id="5b7fe-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5b7fe-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="5b7fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="5b7fe-103">A titkosító kulcs tulajdonságait állítja be egy Snapshot Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="5b7fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b7fe-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b7fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b7fe-105">DESCRIPTION</span></span>
<span data-ttu-id="5b7fe-106">A **set-AzSnapshotUpdateDiskEncryptionKey** parancsmag a titkosító kulcs tulajdonságait a Snapshot Update objektumban állítja be.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="5b7fe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5b7fe-107">EXAMPLES</span></span>

### <span data-ttu-id="5b7fe-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5b7fe-108">Example 1</span></span>
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

<span data-ttu-id="5b7fe-109">Az első parancs létrehoz egy helyi üres Snapshot Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="5b7fe-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5b7fe-111">A második és a harmadik parancs beállítja a merevlemez titkosítási kulcsát és a fontos titkosítási kulcs beállításait a Snapshot Update objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="5b7fe-112">Az utolsó parancs átveszi a Snapshot Update objektumát, és frissíti a "Snapshot01" nevű meglévő pillanatképet az "ResourceGroup01" erőforráscsoport csoportjában.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5b7fe-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b7fe-113">PARAMETERS</span></span>

### <span data-ttu-id="5b7fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b7fe-114">-DefaultProfile</span></span>
<span data-ttu-id="5b7fe-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b7fe-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="5b7fe-116">-SecretUrl</span></span>
<span data-ttu-id="5b7fe-117">Specifes a titkos URL-címet.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-117">Specifes the secret Url.</span></span>

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

### <span data-ttu-id="5b7fe-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5b7fe-118">-SnapshotUpdate</span></span>
<span data-ttu-id="5b7fe-119">Egy helyi Snapshot Update-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b7fe-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5b7fe-120">-SourceVaultId</span></span>
<span data-ttu-id="5b7fe-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="5b7fe-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b7fe-122">-Confirm</span></span>
<span data-ttu-id="5b7fe-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b7fe-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b7fe-124">-WhatIf</span></span>
<span data-ttu-id="5b7fe-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b7fe-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b7fe-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b7fe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b7fe-127">CommonParameters</span></span>
<span data-ttu-id="5b7fe-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b7fe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b7fe-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b7fe-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b7fe-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7fe-130">INPUTS</span></span>

### <span data-ttu-id="5b7fe-131">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5b7fe-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="5b7fe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5b7fe-132">System.String</span></span>

## <span data-ttu-id="5b7fe-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b7fe-133">OUTPUTS</span></span>

### <span data-ttu-id="5b7fe-134">Microsoft. Azure. commands. számítási. Automation. models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5b7fe-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="5b7fe-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b7fe-135">NOTES</span></span>

## <span data-ttu-id="5b7fe-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b7fe-136">RELATED LINKS</span></span>
