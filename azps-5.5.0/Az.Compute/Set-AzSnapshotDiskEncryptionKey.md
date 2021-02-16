---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: e4ecb281382af308176f47462e086f69c18e6163
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166426"
---
# <span data-ttu-id="77508-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="77508-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="77508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77508-102">SYNOPSIS</span></span>
<span data-ttu-id="77508-103">Beállítja a lemeztitkosítási kulcs tulajdonságait egy pillanatfelvételi objektumon.</span><span class="sxs-lookup"><span data-stu-id="77508-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="77508-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77508-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77508-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77508-105">DESCRIPTION</span></span>
<span data-ttu-id="77508-106">A **Set-AzSnapshotDiskEncryptionKey** parancsmag beállítja a lemeztitkosítási kulcs tulajdonságait egy pillanatfelvételi objektumon.</span><span class="sxs-lookup"><span data-stu-id="77508-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="77508-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77508-107">EXAMPLES</span></span>

### <span data-ttu-id="77508-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="77508-108">Example 1</span></span>
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

<span data-ttu-id="77508-109">Az első parancs létrehoz egy 5 GB-os méretű helyi üres pillanatfelvételi objektumot Standard_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="77508-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="77508-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="77508-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="77508-111">A második és a harmadik parancs a pillanatfelvételi objektum lemeztitkosítási és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="77508-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="77508-112">Az utolsó parancs a pillanatfelvételi objektumot a "Snapshot01" néven hozza létre az Erőforráscsoport01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="77508-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="77508-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77508-113">PARAMETERS</span></span>

### <span data-ttu-id="77508-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77508-114">-DefaultProfile</span></span>
<span data-ttu-id="77508-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="77508-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77508-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="77508-116">-SecretUrl</span></span>
<span data-ttu-id="77508-117">A titkos URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="77508-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="77508-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="77508-118">-Snapshot</span></span>
<span data-ttu-id="77508-119">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="77508-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="77508-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="77508-120">-SourceVaultId</span></span>
<span data-ttu-id="77508-121">A forrástár azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="77508-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="77508-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77508-122">-Confirm</span></span>
<span data-ttu-id="77508-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="77508-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77508-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77508-124">-WhatIf</span></span>
<span data-ttu-id="77508-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="77508-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77508-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77508-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77508-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77508-127">CommonParameters</span></span>
<span data-ttu-id="77508-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77508-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77508-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77508-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77508-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77508-130">INPUTS</span></span>

### <span data-ttu-id="77508-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="77508-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="77508-132">System.String</span><span class="sxs-lookup"><span data-stu-id="77508-132">System.String</span></span>

## <span data-ttu-id="77508-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77508-133">OUTPUTS</span></span>

### <span data-ttu-id="77508-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="77508-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="77508-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77508-135">NOTES</span></span>

## <span data-ttu-id="77508-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77508-136">RELATED LINKS</span></span>
