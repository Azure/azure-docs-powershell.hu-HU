---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c8a3ce4f0e21ac12f73fbcef6a4cb6c3b6b65bad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370381"
---
# <span data-ttu-id="de57b-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="de57b-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="de57b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de57b-102">SYNOPSIS</span></span>
<span data-ttu-id="de57b-103">Beállítja a kulcstitkosítási kulcs tulajdonságait egy pillanatfelvételi objektumon.</span><span class="sxs-lookup"><span data-stu-id="de57b-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="de57b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="de57b-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de57b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="de57b-105">DESCRIPTION</span></span>
<span data-ttu-id="de57b-106">A **Set-AzSnapshotKeyEncryptionKey** parancsmag beállítja a kulcstitkosítási kulcs tulajdonságait egy pillanatfelvételi objektumon.</span><span class="sxs-lookup"><span data-stu-id="de57b-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="de57b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="de57b-107">EXAMPLES</span></span>

### <span data-ttu-id="de57b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="de57b-108">Example 1</span></span>
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

<span data-ttu-id="de57b-109">Az első parancs létrehoz egy 5 GB-os méretű helyi üres pillanatfelvételi objektumot Standard_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="de57b-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="de57b-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="de57b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="de57b-111">A második és a harmadik parancs a pillanatfelvételi objektum lemeztitkosítási és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="de57b-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="de57b-112">Az utolsó parancs a pillanatfelvételi objektumot a "Snapshot01" néven hozza létre az Erőforráscsoport01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="de57b-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="de57b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de57b-113">PARAMETERS</span></span>

### <span data-ttu-id="de57b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de57b-114">-DefaultProfile</span></span>
<span data-ttu-id="de57b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="de57b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de57b-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="de57b-116">-KeyUrl</span></span>
<span data-ttu-id="de57b-117">A kulcs URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="de57b-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="de57b-118">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="de57b-118">-Snapshot</span></span>
<span data-ttu-id="de57b-119">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="de57b-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="de57b-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="de57b-120">-SourceVaultId</span></span>
<span data-ttu-id="de57b-121">A forrástár azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="de57b-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="de57b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de57b-122">-Confirm</span></span>
<span data-ttu-id="de57b-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="de57b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de57b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de57b-124">-WhatIf</span></span>
<span data-ttu-id="de57b-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="de57b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de57b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="de57b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de57b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de57b-127">CommonParameters</span></span>
<span data-ttu-id="de57b-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de57b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de57b-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de57b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de57b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de57b-130">INPUTS</span></span>

### <span data-ttu-id="de57b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="de57b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="de57b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="de57b-132">System.String</span></span>

## <span data-ttu-id="de57b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="de57b-133">OUTPUTS</span></span>

### <span data-ttu-id="de57b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="de57b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="de57b-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="de57b-135">NOTES</span></span>

## <span data-ttu-id="de57b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="de57b-136">RELATED LINKS</span></span>
