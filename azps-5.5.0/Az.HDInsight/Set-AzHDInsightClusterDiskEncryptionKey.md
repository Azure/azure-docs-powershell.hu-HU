---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167426"
---
# <span data-ttu-id="eca8b-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="eca8b-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="eca8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eca8b-102">SYNOPSIS</span></span>
<span data-ttu-id="eca8b-103">A megadott HDInsight-fürt lemeztitkosítási kulcsának elforgatása.</span><span class="sxs-lookup"><span data-stu-id="eca8b-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="eca8b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eca8b-104">SYNTAX</span></span>

### <span data-ttu-id="eca8b-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eca8b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca8b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eca8b-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eca8b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eca8b-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eca8b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eca8b-108">DESCRIPTION</span></span>
<span data-ttu-id="eca8b-109">Forgassa el a megadott HDInsight-fürt lemeztitkosítási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="eca8b-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="eca8b-110">A művelethez a fürtnek mind az aktuális, mind a kívánt új kulcshoz hozzáféréssel kell hozzáféréssel lennie, ellenkező esetben az elforgatásbillentyűvel kapcsolatos művelet sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="eca8b-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="eca8b-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eca8b-111">EXAMPLES</span></span>

### <span data-ttu-id="eca8b-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="eca8b-112">Example 1</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterResourceGroupName = "Group"
        $clusterName = "your-cmk-cluster"

Set-AzHDInsightClusterDiskEncryptionKey `
        -ResourceGroupName $clusterResourceGroupName `
        -ClusterName $clusterName `
        -EncryptionKeyName new-key `
        -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
        -EncryptionKeyVersion 00000000000000000000000000000000
```

### <span data-ttu-id="eca8b-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="eca8b-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="eca8b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eca8b-114">PARAMETERS</span></span>

### <span data-ttu-id="eca8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eca8b-115">-DefaultProfile</span></span>
<span data-ttu-id="eca8b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eca8b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eca8b-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="eca8b-117">-EncryptionKeyName</span></span>
<span data-ttu-id="eca8b-118">Beállítja vagy beállítja a titkosítási kulcs nevét.</span><span class="sxs-lookup"><span data-stu-id="eca8b-118">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca8b-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="eca8b-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="eca8b-120">Beállítja vagy beállítja a titkosítási kulcs verzióját.</span><span class="sxs-lookup"><span data-stu-id="eca8b-120">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca8b-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="eca8b-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="eca8b-122">Beállítja vagy beállítja a titkosítási tároló uri-ját.</span><span class="sxs-lookup"><span data-stu-id="eca8b-122">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca8b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eca8b-123">-InputObject</span></span>
<span data-ttu-id="eca8b-124">Beállítja vagy beállítja a bemeneti objektumot.</span><span class="sxs-lookup"><span data-stu-id="eca8b-124">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eca8b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="eca8b-125">-Name</span></span>
<span data-ttu-id="eca8b-126">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="eca8b-126">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca8b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eca8b-127">-ResourceGroupName</span></span>
<span data-ttu-id="eca8b-128">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="eca8b-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eca8b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eca8b-129">-ResourceId</span></span>
<span data-ttu-id="eca8b-130">Beállítja vagy beállítja az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="eca8b-130">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eca8b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eca8b-131">-Confirm</span></span>
<span data-ttu-id="eca8b-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="eca8b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eca8b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eca8b-133">-WhatIf</span></span>
<span data-ttu-id="eca8b-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="eca8b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eca8b-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="eca8b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eca8b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eca8b-136">CommonParameters</span></span>
<span data-ttu-id="eca8b-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eca8b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eca8b-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eca8b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eca8b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eca8b-139">INPUTS</span></span>

### <span data-ttu-id="eca8b-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="eca8b-140">None</span></span>

## <span data-ttu-id="eca8b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eca8b-141">OUTPUTS</span></span>

### <span data-ttu-id="eca8b-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="eca8b-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="eca8b-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eca8b-143">NOTES</span></span>

## <span data-ttu-id="eca8b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eca8b-144">RELATED LINKS</span></span>

[<span data-ttu-id="eca8b-145">Ügyfél által kezelt kulcs lemeztitkosítás</span><span class="sxs-lookup"><span data-stu-id="eca8b-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
