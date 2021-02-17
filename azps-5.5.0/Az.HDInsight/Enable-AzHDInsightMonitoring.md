---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightmonitoring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightMonitoring.md
ms.openlocfilehash: 7ec91d5ab23322185c2920655410b39e2d1a1dce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147827"
---
# <span data-ttu-id="a31e9-101">Enable-AzHDInsightMonitoring</span><span class="sxs-lookup"><span data-stu-id="a31e9-101">Enable-AzHDInsightMonitoring</span></span>

## <span data-ttu-id="a31e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a31e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a31e9-103">A HDInsight-fürtben való figyelés engedélyezése és a kapcsolódó naplók az engedélyezés során megadott figyelési munkaterületre lesznek küldve.</span><span class="sxs-lookup"><span data-stu-id="a31e9-103">Enables monitoring in a HDInsight cluster and relevant logs will be sent to the monitoring workspace specified during enable.</span></span>

## <span data-ttu-id="a31e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a31e9-104">SYNTAX</span></span>

```
Enable-AzHDInsightMonitoring [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a31e9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a31e9-105">DESCRIPTION</span></span>
<span data-ttu-id="a31e9-106">Az **Enable-AzHDInsightMonitoring** parancsmag lehetővé teszi a figyelést az Azure HDInsight-fürtben.</span><span class="sxs-lookup"><span data-stu-id="a31e9-106">The **Enable-AzHDInsightMonitoring** cmdlet enables monitoring in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a31e9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a31e9-107">EXAMPLES</span></span>

### <span data-ttu-id="a31e9-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a31e9-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="a31e9-109">A HDInsight-fürtben engedélyezve lesz a figyelés, és a kapcsolódó naplókat a figyelési munkaterületre küldjük az 1d364e89-bb71-4503-aa3d-a23535aea7bd azonosítóval</span><span class="sxs-lookup"><span data-stu-id="a31e9-109">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="a31e9-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="a31e9-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightMonitoring -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

True
```

<span data-ttu-id="a31e9-111">A HDInsight-fürtben engedélyezve lesz a figyelés, és a kapcsolódó naplókat a figyelési munkaterületre küldjük az 1d364e89-bb71-4503-aa3d-a23535aea7bd azonosítóval</span><span class="sxs-lookup"><span data-stu-id="a31e9-111">Monitoring will be enabled on the HDInsight cluster and relevant logs will be sent to the monitoring workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="a31e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a31e9-112">PARAMETERS</span></span>

### <span data-ttu-id="a31e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31e9-113">-DefaultProfile</span></span>
<span data-ttu-id="a31e9-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a31e9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a31e9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a31e9-115">-Name</span></span>
<span data-ttu-id="a31e9-116">A figyelés engedélyezésére képes fürt neve.</span><span class="sxs-lookup"><span data-stu-id="a31e9-116">The name of the cluster to enable monitoring.</span></span>

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

### <span data-ttu-id="a31e9-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a31e9-117">-PrimaryKey</span></span>
<span data-ttu-id="a31e9-118">A figyelési munkaterület elsődleges kulcsa.</span><span class="sxs-lookup"><span data-stu-id="a31e9-118">The primary key of the monitoring workspace.</span></span>

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

### <span data-ttu-id="a31e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="a31e9-120">A fürt erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="a31e9-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="a31e9-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a31e9-121">-WorkspaceId</span></span>
<span data-ttu-id="a31e9-122">A figyelési munkaterület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a31e9-122">The id of the monitoring workspace.</span></span>

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

### <span data-ttu-id="a31e9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a31e9-123">-Confirm</span></span>
<span data-ttu-id="a31e9-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a31e9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a31e9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a31e9-125">-WhatIf</span></span>
<span data-ttu-id="a31e9-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a31e9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a31e9-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a31e9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a31e9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31e9-128">CommonParameters</span></span>
<span data-ttu-id="a31e9-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31e9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31e9-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a31e9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31e9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a31e9-131">INPUTS</span></span>

### <span data-ttu-id="a31e9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a31e9-132">System.String</span></span>

## <span data-ttu-id="a31e9-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a31e9-133">OUTPUTS</span></span>

### <span data-ttu-id="a31e9-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a31e9-134">System.Boolean</span></span>

## <span data-ttu-id="a31e9-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a31e9-135">NOTES</span></span>

## <span data-ttu-id="a31e9-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a31e9-136">RELATED LINKS</span></span>
