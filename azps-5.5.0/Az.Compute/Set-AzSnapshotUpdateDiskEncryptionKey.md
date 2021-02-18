---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204766"
---
# <span data-ttu-id="9c1ec-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9c1ec-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="9c1ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="9c1ec-103">Beállítja a lemeztitkosítási kulcs tulajdonságait egy pillanatfelvételi frissítési objektumon.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="9c1ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9c1ec-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c1ec-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9c1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="9c1ec-106">A **Set-AzSnapshotUpdateDiskEncryptionKey** parancsmag beállítja a lemeztitkosítási kulcs tulajdonságait egy pillanatfelvételi frissítési objektumon.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="9c1ec-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9c1ec-107">EXAMPLES</span></span>

### <span data-ttu-id="9c1ec-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="9c1ec-108">Example 1</span></span>
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

<span data-ttu-id="9c1ec-109">Az első parancs létrehoz egy 10 GB-os helyi üres pillanatkép-frissítő objektumot Premium_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="9c1ec-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="9c1ec-111">A második és a harmadik parancs a lemeztitkosítási kulcs és a kulcstitkosítási kulcs beállításait adja meg a pillanatfelvételi frissítési objektumhoz.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="9c1ec-112">Az utolsó parancs az "Erőforráscsoport01" erőforráscsoport pillanatkép-frissítő objektumában egy "Snapshot01" nevű pillanatképet frissít.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9c1ec-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c1ec-113">PARAMETERS</span></span>

### <span data-ttu-id="9c1ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c1ec-114">-DefaultProfile</span></span>
<span data-ttu-id="9c1ec-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c1ec-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="9c1ec-116">-SecretUrl</span></span>
<span data-ttu-id="9c1ec-117">A titkos URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="9c1ec-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="9c1ec-118">-SnapshotUpdate</span></span>
<span data-ttu-id="9c1ec-119">Helyi pillanatkép-frissítő objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="9c1ec-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="9c1ec-120">-SourceVaultId</span></span>
<span data-ttu-id="9c1ec-121">A forrástár azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="9c1ec-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c1ec-122">-Confirm</span></span>
<span data-ttu-id="9c1ec-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c1ec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c1ec-124">-WhatIf</span></span>
<span data-ttu-id="9c1ec-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c1ec-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c1ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c1ec-127">CommonParameters</span></span>
<span data-ttu-id="9c1ec-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c1ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c1ec-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c1ec-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c1ec-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9c1ec-130">INPUTS</span></span>

### <span data-ttu-id="9c1ec-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="9c1ec-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="9c1ec-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9c1ec-132">System.String</span></span>

## <span data-ttu-id="9c1ec-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c1ec-133">OUTPUTS</span></span>

### <span data-ttu-id="9c1ec-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="9c1ec-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="9c1ec-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9c1ec-135">NOTES</span></span>

## <span data-ttu-id="9c1ec-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c1ec-136">RELATED LINKS</span></span>
