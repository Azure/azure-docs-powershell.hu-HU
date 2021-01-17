---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469697"
---
# <span data-ttu-id="7aa4f-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="7aa4f-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="7aa4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aa4f-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa4f-103">A HDInsight-fürtben való figyelés engedélyezése és a kapcsolódó naplók az engedélyezés során megadott figyelési munkaterületre lesznek küldve.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="7aa4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7aa4f-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7aa4f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7aa4f-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa4f-106">Az **Enable-AzHDInsightMonitoring** parancsmag lehetővé teszi a figyelést az Azure HDInsight-fürtben.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7aa4f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7aa4f-107">EXAMPLES</span></span>

### <span data-ttu-id="7aa4f-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7aa4f-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="7aa4f-109">A HDInsight-fürtben engedélyezve lesz a figyelés, és a kapcsolódó naplókat a figyelési munkaterületre küldjük az 1d364e89-bb71-4503-aa3d-a23535aea7bd azonosítóval</span><span class="sxs-lookup"><span data-stu-id="7aa4f-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="7aa4f-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="7aa4f-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="7aa4f-111">A HDInsight-fürtben engedélyezve lesz a figyelés, és a kapcsolódó naplókat a figyelési munkaterületre küldjük az 1d364e89-bb71-4503-aa3d-a23535aea7bd azonosítóval</span><span class="sxs-lookup"><span data-stu-id="7aa4f-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="7aa4f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7aa4f-112">PARAMETERS</span></span>

### <span data-ttu-id="7aa4f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa4f-113">-DefaultProfile</span></span>
<span data-ttu-id="7aa4f-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7aa4f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7aa4f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7aa4f-115">-Name</span></span>
<span data-ttu-id="7aa4f-116">A figyelés engedélyezésére képes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="7aa4f-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7aa4f-117">-PrimaryKey</span></span>
<span data-ttu-id="7aa4f-118">A figyelési munkaterület elsődleges kulcsa.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="7aa4f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa4f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7aa4f-120">A fürt erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="7aa4f-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7aa4f-121">-WorkspaceId</span></span>
<span data-ttu-id="7aa4f-122">A figyelési munkaterület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="7aa4f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7aa4f-123">-Confirm</span></span>
<span data-ttu-id="7aa4f-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aa4f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa4f-125">-WhatIf</span></span>
<span data-ttu-id="7aa4f-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7aa4f-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aa4f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa4f-128">CommonParameters</span></span>
<span data-ttu-id="7aa4f-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa4f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa4f-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7aa4f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa4f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7aa4f-131">INPUTS</span></span>

### <span data-ttu-id="7aa4f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7aa4f-132">System.String</span></span>

## <span data-ttu-id="7aa4f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7aa4f-133">OUTPUTS</span></span>

### <span data-ttu-id="7aa4f-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7aa4f-134">System.Boolean</span></span>

## <span data-ttu-id="7aa4f-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7aa4f-135">NOTES</span></span>

## <span data-ttu-id="7aa4f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7aa4f-136">RELATED LINKS</span></span>
