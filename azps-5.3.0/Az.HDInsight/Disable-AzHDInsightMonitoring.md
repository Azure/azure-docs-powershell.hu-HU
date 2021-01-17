---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466074"
---
# <span data-ttu-id="1ea66-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="1ea66-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="1ea66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ea66-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea66-103">A HDInsight-fürtben való figyelés letiltása és a kapcsolódó naplók az engedélyezés során megadott figyelési munkaterületre fognak áramni.</span><span class="sxs-lookup"><span data-stu-id="1ea66-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="1ea66-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1ea66-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ea66-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1ea66-105">DESCRIPTION</span></span>
<span data-ttu-id="1ea66-106">A **Disable-AzHDInsightMonitoring** parancsmag letiltja a figyelés az Azure HDInsight-fürtben.</span><span class="sxs-lookup"><span data-stu-id="1ea66-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1ea66-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1ea66-107">EXAMPLES</span></span>

### <span data-ttu-id="1ea66-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="1ea66-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="1ea66-109">A HDInsight-fürtben le lesz tiltva a figyelés, és a kapcsolódó naplók nem fognak tovább áramlni a figyelési munkaterületre.</span><span class="sxs-lookup"><span data-stu-id="1ea66-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="1ea66-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="1ea66-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="1ea66-111">A HDInsight-fürtben le lesz tiltva a figyelés, és a kapcsolódó naplók nem fognak tovább áramlni a figyelési munkaterületre.</span><span class="sxs-lookup"><span data-stu-id="1ea66-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="1ea66-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ea66-112">PARAMETERS</span></span>

### <span data-ttu-id="1ea66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea66-113">-DefaultProfile</span></span>
<span data-ttu-id="1ea66-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1ea66-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ea66-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1ea66-115">-Name</span></span>
<span data-ttu-id="1ea66-116">Annak a fürtnek a neve, amely letiltja a figyelés letiltását.</span><span class="sxs-lookup"><span data-stu-id="1ea66-116">The name of the cluster to disable Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea66-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ea66-118">A fürt erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="1ea66-118">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea66-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ea66-119">-Confirm</span></span>
<span data-ttu-id="1ea66-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1ea66-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ea66-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ea66-121">-WhatIf</span></span>
<span data-ttu-id="1ea66-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1ea66-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ea66-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ea66-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ea66-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea66-124">CommonParameters</span></span>
<span data-ttu-id="1ea66-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ea66-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea66-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ea66-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea66-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ea66-127">INPUTS</span></span>

### <span data-ttu-id="1ea66-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1ea66-128">System.String</span></span>

## <span data-ttu-id="1ea66-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ea66-129">OUTPUTS</span></span>

### <span data-ttu-id="1ea66-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ea66-130">System.Boolean</span></span>

## <span data-ttu-id="1ea66-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1ea66-131">NOTES</span></span>

## <span data-ttu-id="1ea66-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ea66-132">RELATED LINKS</span></span>
