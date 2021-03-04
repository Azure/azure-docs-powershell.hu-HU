---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightScriptActionHistory.md
ms.openlocfilehash: 8273ad77091d008bead41e568f6c9d2de0e0d6f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934177"
---
# <span data-ttu-id="2d464-101">Get-AzHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="2d464-101">Get-AzHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="2d464-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d464-102">SYNOPSIS</span></span>
<span data-ttu-id="2d464-103">Lekérte egy fürt parancsfájl-műveletelőzményét, és fordított időrendi sorrendben listázza azt, vagy egy korábban végrehajtott parancsprogram-művelet részleteit.</span><span class="sxs-lookup"><span data-stu-id="2d464-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="2d464-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2d464-104">SYNTAX</span></span>

```
Get-AzHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d464-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2d464-105">DESCRIPTION</span></span>
<span data-ttu-id="2d464-106">A **Get-AzHDInsightScriptActionHistory** parancsmag begyűjte egy Azure HDInsight-fürt parancsfájl-műveletelőzményeit, és fordított időrendi sorrendben listázza azt, vagy egy korábban végrehajtott parancsfájl-művelet részleteit.</span><span class="sxs-lookup"><span data-stu-id="2d464-106">The **Get-AzHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="2d464-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2d464-107">EXAMPLES</span></span>

### <span data-ttu-id="2d464-108">1. példa: A parancsfájl-műveletek végrehajtásának előzményeinek lekérte egy fürtre</span><span class="sxs-lookup"><span data-stu-id="2d464-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="2d464-109">Ez a parancs a parancsfájl-műveletek előzményeit kapja meg a -hadoop-001-es fürthöz.</span><span class="sxs-lookup"><span data-stu-id="2d464-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="2d464-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d464-110">PARAMETERS</span></span>

### <span data-ttu-id="2d464-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2d464-111">-ClusterName</span></span>
<span data-ttu-id="2d464-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d464-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2d464-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d464-113">-DefaultProfile</span></span>
<span data-ttu-id="2d464-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d464-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d464-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d464-115">-ResourceGroupName</span></span>
<span data-ttu-id="2d464-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d464-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2d464-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="2d464-117">-ScriptExecutionId</span></span>
<span data-ttu-id="2d464-118">A végrehajtott parancsfájl-művelet végrehajtási azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d464-118">Specifies the execution ID of the executed script action.</span></span>

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

### <span data-ttu-id="2d464-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d464-119">CommonParameters</span></span>
<span data-ttu-id="2d464-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d464-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d464-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d464-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d464-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d464-122">INPUTS</span></span>

### <span data-ttu-id="2d464-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="2d464-123">None</span></span>

## <span data-ttu-id="2d464-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d464-124">OUTPUTS</span></span>

### <span data-ttu-id="2d464-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span><span class="sxs-lookup"><span data-stu-id="2d464-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail</span></span>

## <span data-ttu-id="2d464-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2d464-126">NOTES</span></span>

## <span data-ttu-id="2d464-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d464-127">RELATED LINKS</span></span>
