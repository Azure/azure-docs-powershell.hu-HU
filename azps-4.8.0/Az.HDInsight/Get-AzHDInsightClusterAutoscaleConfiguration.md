---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025714"
---
# <span data-ttu-id="91346-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="91346-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="91346-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91346-102">SYNOPSIS</span></span>
<span data-ttu-id="91346-103">Beilleszti a HDInsight-fürt automatikus méretarányos konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="91346-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="91346-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91346-104">SYNTAX</span></span>

### <span data-ttu-id="91346-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91346-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91346-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91346-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91346-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="91346-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91346-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91346-108">DESCRIPTION</span></span>
<span data-ttu-id="91346-109">A **Get-AzHDInsightClusterAutoscaleConfiguration** parancsmag az HDInsight-fürtök automatikus méretezési konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="91346-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="91346-110">Példák</span><span class="sxs-lookup"><span data-stu-id="91346-110">EXAMPLES</span></span>

### <span data-ttu-id="91346-111">Példa 1: a HDInsight-fürt automatikus méretezési konfigurációjának beszerzése.</span><span class="sxs-lookup"><span data-stu-id="91346-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="91346-112">Ez a parancs beilleszti az HDInsight-fürt automatikus méretarányos konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="91346-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="91346-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91346-113">PARAMETERS</span></span>

### <span data-ttu-id="91346-114">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="91346-114">-ClusterName</span></span>
<span data-ttu-id="91346-115">A fürt nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="91346-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91346-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91346-116">-DefaultProfile</span></span>
<span data-ttu-id="91346-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91346-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91346-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91346-118">-InputObject</span></span>
<span data-ttu-id="91346-119">A beviteli objektum beolvasása vagy megadása</span><span class="sxs-lookup"><span data-stu-id="91346-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91346-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91346-120">-ResourceGroupName</span></span>
<span data-ttu-id="91346-121">Az erőforráscsoport nevének beolvasása vagy megadására szolgáló parancs.</span><span class="sxs-lookup"><span data-stu-id="91346-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91346-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91346-122">-ResourceId</span></span>
<span data-ttu-id="91346-123">Az erőforrás azonosítóját kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="91346-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91346-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91346-124">CommonParameters</span></span>
<span data-ttu-id="91346-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91346-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91346-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91346-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91346-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91346-127">INPUTS</span></span>

### <span data-ttu-id="91346-128">System. String</span><span class="sxs-lookup"><span data-stu-id="91346-128">System.String</span></span>

### <span data-ttu-id="91346-129">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="91346-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="91346-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91346-130">OUTPUTS</span></span>

### <span data-ttu-id="91346-131">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="91346-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="91346-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91346-132">NOTES</span></span>

## <span data-ttu-id="91346-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91346-133">RELATED LINKS</span></span>

<span data-ttu-id="91346-134">[Új – AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="91346-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
