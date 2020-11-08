---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightMonitoring.md
ms.openlocfilehash: 9a65a82808c78fe878ba4a61f8be01f37fc11771
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185380"
---
# <span data-ttu-id="dcfbf-101">Disable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="dcfbf-101">Disable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="dcfbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dcfbf-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfbf-103">Letiltja a figyelést egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott figyelési munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-103">Disables monitoring in a HDInsight cluster and relevant logs will stop flowing to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="dcfbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dcfbf-104">SYNTAX</span></span>

```
Disable-AzHDInsightMonitoring [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcfbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dcfbf-105">DESCRIPTION</span></span>
<span data-ttu-id="dcfbf-106">A **disable-AzHDInsightMonitoring** parancsmag letiltja a figyelést az Azure HDInsight-fürtökben.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-106">The **Disable-AzHDInsightMonitoring** cmdlet disables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="dcfbf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dcfbf-107">EXAMPLES</span></span>

### <span data-ttu-id="dcfbf-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dcfbf-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster

True
```

<span data-ttu-id="dcfbf-109">A figyelés le lesz tiltva a HDInsight-fürtben, és a fontos naplók a figyelési munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-109">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

### <span data-ttu-id="dcfbf-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="dcfbf-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg

True
```

<span data-ttu-id="dcfbf-111">A figyelés le lesz tiltva a HDInsight-fürtben, és a fontos naplók a figyelési munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-111">Monitoring will be disabled on the HDInsight cluster and relevant logs will stop flowing to the monitoring workspace.</span></span>

## <span data-ttu-id="dcfbf-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dcfbf-112">PARAMETERS</span></span>

### <span data-ttu-id="dcfbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfbf-113">-DefaultProfile</span></span>
<span data-ttu-id="dcfbf-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dcfbf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcfbf-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dcfbf-115">-Name</span></span>
<span data-ttu-id="dcfbf-116">Annak a fürtnek a neve, amelyből le szeretné tiltani a figyelést.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-116">The name of the cluster to disable Monitoring.</span></span>

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

### <span data-ttu-id="dcfbf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcfbf-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcfbf-118">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="dcfbf-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="dcfbf-119">-Confirm</span></span>
<span data-ttu-id="dcfbf-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcfbf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcfbf-121">-WhatIf</span></span>
<span data-ttu-id="dcfbf-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcfbf-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcfbf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfbf-124">CommonParameters</span></span>
<span data-ttu-id="dcfbf-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dcfbf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcfbf-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="dcfbf-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfbf-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcfbf-127">INPUTS</span></span>

### <span data-ttu-id="dcfbf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dcfbf-128">System.String</span></span>

## <span data-ttu-id="dcfbf-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcfbf-129">OUTPUTS</span></span>

### <span data-ttu-id="dcfbf-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dcfbf-130">System.Boolean</span></span>

## <span data-ttu-id="dcfbf-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dcfbf-131">NOTES</span></span>

## <span data-ttu-id="dcfbf-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcfbf-132">RELATED LINKS</span></span>