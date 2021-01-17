---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: f22a5b4bc9b30e152827f1914bd03a4a6cee4971
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350261"
---
# <span data-ttu-id="0e2d1-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="0e2d1-101">New-AzSnapshot</span></span>

## <span data-ttu-id="0e2d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2d1-103">Pillanatképet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-103">Creates a snapshot.</span></span>

## <span data-ttu-id="0e2d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e2d1-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e2d1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e2d1-105">DESCRIPTION</span></span>
<span data-ttu-id="0e2d1-106">A **New-AzSnapshot** parancsmag pillanatképet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="0e2d1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e2d1-107">EXAMPLES</span></span>

### <span data-ttu-id="0e2d1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="0e2d1-108">Example 1</span></span>
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

<span data-ttu-id="0e2d1-109">Az első parancs létrehoz egy 5 GB-os méretű helyi üres pillanatfelvételi objektumot Standard_LRS tárfiók típusában.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0e2d1-110">Emellett beállítja a Windows operációs rendszer típusát, és engedélyezi a titkosítási beállításokat.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0e2d1-111">A második és a harmadik parancs a pillanatfelvételi objektum lemeztitkosítási és kulcstitkosítási kulcsának beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="0e2d1-112">Az utolsó parancs a pillanatfelvételi objektumot a "Snapshot01" néven hozza létre az Erőforráscsoport01 erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0e2d1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e2d1-113">PARAMETERS</span></span>

### <span data-ttu-id="0e2d1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e2d1-114">-AsJob</span></span>
<span data-ttu-id="0e2d1-115">Futtasa a parancsmagot a háttérben, és adja vissza a feladatot az előrehaladás nyomon követéséhez.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2d1-116">-DefaultProfile</span></span>
<span data-ttu-id="0e2d1-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e2d1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e2d1-118">-ResourceGroupName</span></span>
<span data-ttu-id="0e2d1-119">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e2d1-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="0e2d1-120">-Snapshot</span></span>
<span data-ttu-id="0e2d1-121">Helyi pillanatkép-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e2d1-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="0e2d1-122">-SnapshotName</span></span>
<span data-ttu-id="0e2d1-123">Egy pillanatfelvétel nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-123">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e2d1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e2d1-124">-Confirm</span></span>
<span data-ttu-id="0e2d1-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e2d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e2d1-126">-WhatIf</span></span>
<span data-ttu-id="0e2d1-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e2d1-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e2d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2d1-129">CommonParameters</span></span>
<span data-ttu-id="0e2d1-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e2d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e2d1-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e2d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2d1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e2d1-132">INPUTS</span></span>

### <span data-ttu-id="0e2d1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0e2d1-133">System.String</span></span>

### <span data-ttu-id="0e2d1-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0e2d1-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0e2d1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e2d1-135">OUTPUTS</span></span>

### <span data-ttu-id="0e2d1-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0e2d1-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0e2d1-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e2d1-137">NOTES</span></span>

## <span data-ttu-id="0e2d1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e2d1-138">RELATED LINKS</span></span>
