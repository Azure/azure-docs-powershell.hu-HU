---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: addf0e06a3df625bde5b46cc8089fc89ced832dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934953"
---
# <span data-ttu-id="8323f-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8323f-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="8323f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8323f-102">SYNOPSIS</span></span>
<span data-ttu-id="8323f-103">A megadott HDInsight-fürt lemeztitkosítási kulcsának elforgatása.</span><span class="sxs-lookup"><span data-stu-id="8323f-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="8323f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8323f-104">SYNTAX</span></span>

### <span data-ttu-id="8323f-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8323f-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8323f-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8323f-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8323f-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8323f-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8323f-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8323f-108">DESCRIPTION</span></span>
<span data-ttu-id="8323f-109">Forgassa el a megadott HDInsight-fürt lemeztitkosítási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="8323f-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="8323f-110">A művelethez a fürtnek mind az aktuális kulcshoz, mind a kívánt új kulcshoz hozzáféréssel kell hozzáféréssel lennie, ellenkező esetben az elforgatásbillentyű-művelet sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="8323f-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="8323f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8323f-111">EXAMPLES</span></span>

### <span data-ttu-id="8323f-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="8323f-112">Example 1</span></span>
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

### <span data-ttu-id="8323f-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="8323f-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="8323f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8323f-114">PARAMETERS</span></span>

### <span data-ttu-id="8323f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8323f-115">-DefaultProfile</span></span>
<span data-ttu-id="8323f-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8323f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8323f-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="8323f-117">-EncryptionKeyName</span></span>
<span data-ttu-id="8323f-118">Beállítja vagy beállítja a titkosítási kulcs nevét.</span><span class="sxs-lookup"><span data-stu-id="8323f-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="8323f-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="8323f-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="8323f-120">Beállítja vagy beállítja a titkosítási kulcs verzióját.</span><span class="sxs-lookup"><span data-stu-id="8323f-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="8323f-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="8323f-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="8323f-122">Beállítja vagy beállítja a titkosítási tároló uri-ját.</span><span class="sxs-lookup"><span data-stu-id="8323f-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="8323f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8323f-123">-InputObject</span></span>
<span data-ttu-id="8323f-124">Beállítja vagy beállítja a bemeneti objektumot.</span><span class="sxs-lookup"><span data-stu-id="8323f-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="8323f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8323f-125">-Name</span></span>
<span data-ttu-id="8323f-126">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="8323f-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="8323f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8323f-127">-ResourceGroupName</span></span>
<span data-ttu-id="8323f-128">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="8323f-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="8323f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8323f-129">-ResourceId</span></span>
<span data-ttu-id="8323f-130">Beállítja vagy beállítja az erőforrás-azonosítót.</span><span class="sxs-lookup"><span data-stu-id="8323f-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="8323f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8323f-131">-Confirm</span></span>
<span data-ttu-id="8323f-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8323f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8323f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8323f-133">-WhatIf</span></span>
<span data-ttu-id="8323f-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8323f-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8323f-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8323f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8323f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8323f-136">CommonParameters</span></span>
<span data-ttu-id="8323f-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8323f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8323f-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8323f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8323f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8323f-139">INPUTS</span></span>

### <span data-ttu-id="8323f-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="8323f-140">None</span></span>

## <span data-ttu-id="8323f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8323f-141">OUTPUTS</span></span>

### <span data-ttu-id="8323f-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="8323f-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="8323f-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8323f-143">NOTES</span></span>

## <span data-ttu-id="8323f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8323f-144">RELATED LINKS</span></span>

[<span data-ttu-id="8323f-145">Ügyfél által kezelt kulcs lemeztitkosítás</span><span class="sxs-lookup"><span data-stu-id="8323f-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/azure/hdinsight/disk-encryption)
