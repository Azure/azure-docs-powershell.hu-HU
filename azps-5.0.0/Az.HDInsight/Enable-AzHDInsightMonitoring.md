---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185379"
---
# <span data-ttu-id="a3d57-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a3d57-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="a3d57-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3d57-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d57-103">Lehetővé teszi a HDInsight-fürtök figyelését, és a megfelelő naplók az engedélyezés során megadott figyelési munkaterületre kerülnek.</span><span class="sxs-lookup"><span data-stu-id="a3d57-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="a3d57-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3d57-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3d57-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3d57-105">DESCRIPTION</span></span>
<span data-ttu-id="a3d57-106">Az **enable-AzHDInsightMonitoring** parancsmag az Azure HDInsight-fürtök figyelését engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="a3d57-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a3d57-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a3d57-107">EXAMPLES</span></span>

### <span data-ttu-id="a3d57-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a3d57-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="a3d57-109">A figyelés engedélyezve lesz a HDInsight-fürtben, és a megfelelő naplók a figyelési munkaterületre kerülnek a 1d364e89-bb71-4503-aa3d-a23535aea7bd azonosítóval</span><span class="sxs-lookup"><span data-stu-id="a3d57-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a3d57-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="a3d57-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="a3d57-111">A figyelés engedélyezve lesz a HDInsight-fürtben, és a megfelelő naplók a figyelési munkaterületre kerülnek a 1d364e89-bb71-4503-aa3d-a23535aea7bd azonosítóval</span><span class="sxs-lookup"><span data-stu-id="a3d57-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="a3d57-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3d57-112">PARAMETERS</span></span>

### <span data-ttu-id="a3d57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d57-113">-DefaultProfile</span></span>
<span data-ttu-id="a3d57-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3d57-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3d57-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3d57-115">-Name</span></span>
<span data-ttu-id="a3d57-116">Annak a fürtnek a neve, amely lehetővé teszi a figyelést.</span><span class="sxs-lookup"><span data-stu-id="a3d57-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="a3d57-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a3d57-117">-PrimaryKey</span></span>
<span data-ttu-id="a3d57-118">A figyelési munkaterület elsődleges kulcsa.</span><span class="sxs-lookup"><span data-stu-id="a3d57-118">The primary key of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d57-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d57-119">-ResourceGroupName</span></span>
<span data-ttu-id="a3d57-120">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="a3d57-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="a3d57-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a3d57-121">-WorkspaceId</span></span>
<span data-ttu-id="a3d57-122">A figyelési munkaterület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3d57-122">The id of the monitoring workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d57-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3d57-123">-Confirm</span></span>
<span data-ttu-id="a3d57-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3d57-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d57-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d57-125">-WhatIf</span></span>
<span data-ttu-id="a3d57-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3d57-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3d57-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3d57-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d57-128">CommonParameters</span></span>
<span data-ttu-id="a3d57-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3d57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d57-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a3d57-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d57-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3d57-131">INPUTS</span></span>

### <span data-ttu-id="a3d57-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a3d57-132">System.String</span></span>

## <span data-ttu-id="a3d57-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3d57-133">OUTPUTS</span></span>

### <span data-ttu-id="a3d57-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3d57-134">System.Boolean</span></span>

## <span data-ttu-id="a3d57-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3d57-135">NOTES</span></span>

## <span data-ttu-id="a3d57-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3d57-136">RELATED LINKS</span></span>
