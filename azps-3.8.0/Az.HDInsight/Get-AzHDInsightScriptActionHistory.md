---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 4f73c58ee709e53e1337c161b698aa31cc38ca43
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847558"
---
# <span data-ttu-id="9003f-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="9003f-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="9003f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9003f-102">SYNOPSIS</span></span>
<span data-ttu-id="9003f-103">Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9003f-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="9003f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9003f-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9003f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9003f-105">DESCRIPTION</span></span>
<span data-ttu-id="9003f-106">A **Get-AzHDInsightScriptActionHistory parancsmag beolvassa** az Azure HDInsight-fürtök parancsfájl-műveletek előzményeit, és a fordított időrendi sorrendben felsorolja azt, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9003f-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="9003f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9003f-107">EXAMPLES</span></span>

### <span data-ttu-id="9003f-108">Példa 1: egy fürt parancsfájl-végrehajtási műveleteinek előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9003f-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="9003f-109">Ez a parancs a Hadoop-001-alapú fürthöz tartozó parancsfájl-műveletek előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="9003f-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="9003f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9003f-110">PARAMETERS</span></span>

### <span data-ttu-id="9003f-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="9003f-111">-ClusterName</span></span>
<span data-ttu-id="9003f-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9003f-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9003f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9003f-113">-DefaultProfile</span></span>
<span data-ttu-id="9003f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9003f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9003f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9003f-115">-ResourceGroupName</span></span>
<span data-ttu-id="9003f-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9003f-116">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9003f-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="9003f-117">-ScriptExecutionId</span></span>
<span data-ttu-id="9003f-118">A futtatott parancsfájl műveleti AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="9003f-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9003f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9003f-119">CommonParameters</span></span>
<span data-ttu-id="9003f-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9003f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9003f-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9003f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9003f-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9003f-122">INPUTS</span></span>

### <span data-ttu-id="9003f-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="9003f-123">None</span></span>

## <span data-ttu-id="9003f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9003f-124">OUTPUTS</span></span>

### <span data-ttu-id="9003f-125">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="9003f-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="9003f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9003f-126">NOTES</span></span>

## <span data-ttu-id="9003f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9003f-127">RELATED LINKS</span></span>
