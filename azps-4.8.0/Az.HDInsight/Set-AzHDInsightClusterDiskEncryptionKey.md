---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5141D84C-3C58-42B9-890F-C3C9049BC1C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclusterdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterDiskEncryptionKey.md
ms.openlocfilehash: b3421fa4382912d11a3e3a28b81acffb7be123a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183386"
---
# <span data-ttu-id="3bdf3-101">Set-AzHDInsightClusterDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3bdf3-101">Set-AzHDInsightClusterDiskEncryptionKey</span></span>

## <span data-ttu-id="3bdf3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bdf3-102">SYNOPSIS</span></span>
<span data-ttu-id="3bdf3-103">Elforgatja a megadott HDInsight-fürt lemez titkosítási kulcsát.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-103">Rotates the disk encryption key of the specified HDInsight cluster.</span></span>

## <span data-ttu-id="3bdf3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bdf3-104">SYNTAX</span></span>

### <span data-ttu-id="3bdf3-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3bdf3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceGroupName] <String> [-Name] <String>
 -EncryptionKeyName <String> -EncryptionKeyVersion <String> -EncryptionVaultUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bdf3-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bdf3-106">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-ResourceId] <String> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bdf3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3bdf3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightClusterDiskEncryptionKey [-InputObject] <AzureHDInsightCluster> -EncryptionKeyName <String>
 -EncryptionKeyVersion <String> -EncryptionVaultUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bdf3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bdf3-108">DESCRIPTION</span></span>
<span data-ttu-id="3bdf3-109">A megadott HDInsight-fürt lemez-titkosítási kulcsának elforgatása</span><span class="sxs-lookup"><span data-stu-id="3bdf3-109">Rotate the disk encryption key of the specified HDInsight cluster.</span></span> <span data-ttu-id="3bdf3-110">Ehhez a művelethez a fürtnek hozzáféréssel kell rendelkeznie az aktuális kulcshoz és a kívánt új kulcshoz, ellenkező esetben a forgatási művelet sikertelen lesz.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-110">For this operation, the cluster must have access to both the current key and the intended new key, otherwise the rotate key operation will fail.</span></span>

## <span data-ttu-id="3bdf3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3bdf3-111">EXAMPLES</span></span>

### <span data-ttu-id="3bdf3-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3bdf3-112">Example 1</span></span>
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

### <span data-ttu-id="3bdf3-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="3bdf3-113">Example 2</span></span>
```powershell
PS C:\> # Cluster configuration info
        $clusterName = "your-cmk-cluster"

$cluster= Get-AzHDInsightCluster -ClusterName $clusterName 
$cluster |  Set-AzHDInsightClusterDiskEncryptionKey `
    -EncryptionKeyName new-key `
    -EncryptionVaultUri https://MyKeyVault.vault.azure.net `
    -EncryptionKeyVersion 00000000000000000000000000000000
```

## <span data-ttu-id="3bdf3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bdf3-114">PARAMETERS</span></span>

### <span data-ttu-id="3bdf3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bdf3-115">-DefaultProfile</span></span>
<span data-ttu-id="3bdf3-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bdf3-117">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="3bdf3-117">-EncryptionKeyName</span></span>
<span data-ttu-id="3bdf3-118">A titkosítási kulcs nevének beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="3bdf3-118">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="3bdf3-119">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="3bdf3-119">-EncryptionKeyVersion</span></span>
<span data-ttu-id="3bdf3-120">A titkosító kulcs verziójának beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="3bdf3-120">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="3bdf3-121">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="3bdf3-121">-EncryptionVaultUri</span></span>
<span data-ttu-id="3bdf3-122">A titkosítási tároló URI-azonosítójának beolvasása vagy visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-122">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="3bdf3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bdf3-123">-InputObject</span></span>
<span data-ttu-id="3bdf3-124">A beviteli objektum beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="3bdf3-124">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="3bdf3-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3bdf3-125">-Name</span></span>
<span data-ttu-id="3bdf3-126">A fürt nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-126">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="3bdf3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bdf3-127">-ResourceGroupName</span></span>
<span data-ttu-id="3bdf3-128">Az erőforráscsoport nevének beolvasása vagy megadására szolgáló parancs.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="3bdf3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bdf3-129">-ResourceId</span></span>
<span data-ttu-id="3bdf3-130">Az erőforrás azonosítóját kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-130">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="3bdf3-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3bdf3-131">-Confirm</span></span>
<span data-ttu-id="3bdf3-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bdf3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bdf3-133">-WhatIf</span></span>
<span data-ttu-id="3bdf3-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bdf3-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bdf3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bdf3-136">CommonParameters</span></span>
<span data-ttu-id="3bdf3-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bdf3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bdf3-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3bdf3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bdf3-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bdf3-139">INPUTS</span></span>

### <span data-ttu-id="3bdf3-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="3bdf3-140">None</span></span>

## <span data-ttu-id="3bdf3-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bdf3-141">OUTPUTS</span></span>

### <span data-ttu-id="3bdf3-142">Microsoft. Azure. Management. HDInsight. models. cluster</span><span class="sxs-lookup"><span data-stu-id="3bdf3-142">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="3bdf3-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bdf3-143">NOTES</span></span>

## <span data-ttu-id="3bdf3-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bdf3-144">RELATED LINKS</span></span>

[<span data-ttu-id="3bdf3-145">Ügyfél által felügyelt kulcsos merevlemez-titkosítás</span><span class="sxs-lookup"><span data-stu-id="3bdf3-145">Customer-managed key disk encryption</span></span>](https://docs.microsoft.com/en-us/azure/hdinsight/disk-encryption)
