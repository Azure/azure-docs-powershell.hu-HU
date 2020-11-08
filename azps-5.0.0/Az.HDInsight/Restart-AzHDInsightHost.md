---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: d4b184dfbf834822110369e40fbbfb4eb168e424
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187833"
---
# <span data-ttu-id="9dbe9-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="9dbe9-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="9dbe9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9dbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbe9-103">A HDInsight-fürt adott állomásainak újraindítása.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="9dbe9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9dbe9-104">SYNTAX</span></span>

### <span data-ttu-id="9dbe9-105">SetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9dbe9-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [[-DefaultProfile] <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dbe9-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dbe9-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [[-DefaultProfile] <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dbe9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9dbe9-107">DESCRIPTION</span></span>
<span data-ttu-id="9dbe9-108">Ez az **Újraindítás – AzHDInsightHost** parancsmag újraindítja a HDInsight-fürt adott állomásait.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="9dbe9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9dbe9-109">EXAMPLES</span></span>

### <span data-ttu-id="9dbe9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9dbe9-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="9dbe9-111">Ez a parancs a fürt két állomását indítja el: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="9dbe9-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="9dbe9-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="9dbe9-113">Ez a parancs bemutatja, hogyan működhet együtt a "Get-AzHDInsightHost" parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="9dbe9-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9dbe9-114">PARAMETERS</span></span>

### <span data-ttu-id="9dbe9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dbe9-115">-AsJob</span></span>
<span data-ttu-id="9dbe9-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9dbe9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dbe9-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="9dbe9-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="9dbe9-118">Az állomás nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-118">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="9dbe9-119">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="9dbe9-119">-ClusterName</span></span>
<span data-ttu-id="9dbe9-120">A fürt nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="9dbe9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbe9-121">-DefaultProfile</span></span>
<span data-ttu-id="9dbe9-122">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dbe9-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9dbe9-123">-Name</span></span>
<span data-ttu-id="9dbe9-124">Az állomás nevének beolvasása vagy megadására szolgáló beállítás.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-124">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="9dbe9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dbe9-125">-PassThru</span></span>
<span data-ttu-id="9dbe9-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9dbe9-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9dbe9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dbe9-127">-ResourceGroupName</span></span>
<span data-ttu-id="9dbe9-128">Az erőforráscsoport nevének beolvasása vagy megadására szolgáló parancs.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="9dbe9-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9dbe9-129">-Confirm</span></span>
<span data-ttu-id="9dbe9-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dbe9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dbe9-131">-WhatIf</span></span>
<span data-ttu-id="9dbe9-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dbe9-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dbe9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbe9-134">CommonParameters</span></span>
<span data-ttu-id="9dbe9-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9dbe9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbe9-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9dbe9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbe9-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dbe9-137">INPUTS</span></span>

### <span data-ttu-id="9dbe9-138">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. commands. HDInsight. models. Management. AzureHDInsightHostInfo, Microsoft. Azure. PowerShell. parancsmagok. HDInsight, Version = 3.2.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9dbe9-138">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo, Microsoft.Azure.PowerShell.Cmdlets.HDInsight, Version=3.2.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9dbe9-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9dbe9-139">OUTPUTS</span></span>

### <span data-ttu-id="9dbe9-140">Microsoft. Azure. Management. HDInsight. models. cluster</span><span class="sxs-lookup"><span data-stu-id="9dbe9-140">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="9dbe9-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9dbe9-141">NOTES</span></span>

## <span data-ttu-id="9dbe9-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9dbe9-142">RELATED LINKS</span></span>