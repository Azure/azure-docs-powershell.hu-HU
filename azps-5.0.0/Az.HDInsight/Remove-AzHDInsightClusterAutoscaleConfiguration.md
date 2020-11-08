---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187831"
---
# <span data-ttu-id="613d1-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="613d1-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="613d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="613d1-102">SYNOPSIS</span></span>
<span data-ttu-id="613d1-103">Eltávolítja a HDInsight-fürt automatikus méretezési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="613d1-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="613d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="613d1-104">SYNTAX</span></span>

### <span data-ttu-id="613d1-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="613d1-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="613d1-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="613d1-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="613d1-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="613d1-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="613d1-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="613d1-108">DESCRIPTION</span></span>
<span data-ttu-id="613d1-109">A **Remove-AzHDInsightClusterAutoscaleConfiguration** parancsmag eltávolítja a HDInsight-fürt automatikus méretezési konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="613d1-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="613d1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="613d1-110">EXAMPLES</span></span>

### <span data-ttu-id="613d1-111">1. példa: a HDInsight-fürt automatikus méretezési konfigurációjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="613d1-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="613d1-112">Ez a parancs eltávolítja a HDInsight-fürt automatikus méretarányos konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="613d1-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="613d1-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="613d1-113">PARAMETERS</span></span>

### <span data-ttu-id="613d1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="613d1-114">-AsJob</span></span>
<span data-ttu-id="613d1-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="613d1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="613d1-116">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="613d1-116">-ClusterName</span></span>
<span data-ttu-id="613d1-117">A fürt nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="613d1-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="613d1-118">-DefaultProfile</span></span>
<span data-ttu-id="613d1-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="613d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="613d1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="613d1-120">-InputObject</span></span>
<span data-ttu-id="613d1-121">A beviteli objektum beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="613d1-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="613d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="613d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="613d1-123">Az erőforráscsoport nevének beolvasása vagy megadására szolgáló parancs.</span><span class="sxs-lookup"><span data-stu-id="613d1-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613d1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="613d1-124">-ResourceId</span></span>
<span data-ttu-id="613d1-125">Az erőforrás azonosítóját kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="613d1-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613d1-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="613d1-126">-Confirm</span></span>
<span data-ttu-id="613d1-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="613d1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="613d1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="613d1-128">-WhatIf</span></span>
<span data-ttu-id="613d1-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="613d1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="613d1-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="613d1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="613d1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="613d1-131">CommonParameters</span></span>
<span data-ttu-id="613d1-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="613d1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="613d1-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="613d1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="613d1-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="613d1-134">INPUTS</span></span>

### <span data-ttu-id="613d1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="613d1-135">System.String</span></span>

### <span data-ttu-id="613d1-136">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="613d1-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="613d1-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="613d1-137">OUTPUTS</span></span>

### <span data-ttu-id="613d1-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="613d1-138">System.Boolean</span></span>

## <span data-ttu-id="613d1-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="613d1-139">NOTES</span></span>

## <span data-ttu-id="613d1-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="613d1-140">RELATED LINKS</span></span>

<span data-ttu-id="613d1-141">[Új – AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="613d1-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
