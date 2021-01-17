---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: 4e0b5fda29696fb45515c3b478b9dc29ff67263e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322934"
---
# <span data-ttu-id="4aafd-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="4aafd-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="4aafd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aafd-102">SYNOPSIS</span></span>
<span data-ttu-id="4aafd-103">Újraindítja a HDInsight-fürt adott állomását.</span><span class="sxs-lookup"><span data-stu-id="4aafd-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="4aafd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4aafd-104">SYNTAX</span></span>

### <span data-ttu-id="4aafd-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4aafd-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aafd-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aafd-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aafd-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4aafd-107">DESCRIPTION</span></span>
<span data-ttu-id="4aafd-108">Ez **az Restart-AzHDInsightHost** parancsmag újraindítja a HDInsight-fürt adott állomását.</span><span class="sxs-lookup"><span data-stu-id="4aafd-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="4aafd-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4aafd-109">EXAMPLES</span></span>

### <span data-ttu-id="4aafd-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="4aafd-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="4aafd-111">Ez a parancs újraindítja a fürt két állomását: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="4aafd-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="4aafd-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="4aafd-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="4aafd-113">Ez a parancs bemutatja, hogy miként lehet együttműködni a "Get-AzHDInsightHost" parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="4aafd-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="4aafd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aafd-114">PARAMETERS</span></span>

### <span data-ttu-id="4aafd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aafd-115">-AsJob</span></span>
<span data-ttu-id="4aafd-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4aafd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4aafd-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="4aafd-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="4aafd-118">Beállítja vagy beállítja az állomás nevét.</span><span class="sxs-lookup"><span data-stu-id="4aafd-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aafd-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4aafd-119">-ClusterName</span></span>
<span data-ttu-id="4aafd-120">Beállítja vagy beállítja a fürt nevét.</span><span class="sxs-lookup"><span data-stu-id="4aafd-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="4aafd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aafd-121">-DefaultProfile</span></span>
<span data-ttu-id="4aafd-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4aafd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4aafd-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4aafd-123">-Name</span></span>
<span data-ttu-id="4aafd-124">Beállítja vagy beállítja az állomás nevét.</span><span class="sxs-lookup"><span data-stu-id="4aafd-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aafd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4aafd-125">-PassThru</span></span>
<span data-ttu-id="4aafd-126">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="4aafd-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="4aafd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aafd-127">-ResourceGroupName</span></span>
<span data-ttu-id="4aafd-128">Beállítja vagy beállítja az erőforráscsoport nevét.</span><span class="sxs-lookup"><span data-stu-id="4aafd-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aafd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4aafd-129">-Confirm</span></span>
<span data-ttu-id="4aafd-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="4aafd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4aafd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aafd-131">-WhatIf</span></span>
<span data-ttu-id="4aafd-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="4aafd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aafd-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4aafd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4aafd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aafd-134">CommonParameters</span></span>
<span data-ttu-id="4aafd-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aafd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aafd-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aafd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aafd-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4aafd-137">INPUTS</span></span>

### <span data-ttu-id="4aafd-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4aafd-138">System.String[]</span></span>

### <span data-ttu-id="4aafd-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span><span class="sxs-lookup"><span data-stu-id="4aafd-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="4aafd-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aafd-140">OUTPUTS</span></span>

### <span data-ttu-id="4aafd-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4aafd-141">System.Boolean</span></span>

## <span data-ttu-id="4aafd-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4aafd-142">NOTES</span></span>

## <span data-ttu-id="4aafd-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4aafd-143">RELATED LINKS</span></span>
