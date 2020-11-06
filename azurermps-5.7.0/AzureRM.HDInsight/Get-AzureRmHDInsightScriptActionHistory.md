---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: CE690DB0-0CD4-4841-B219-C208173D4730
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightscriptactionhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightScriptActionHistory.md
ms.openlocfilehash: b2e302f9490cb5671728a46105ad574b54270c78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492278"
---
# <span data-ttu-id="cd4c2-101">Get-AzureRmHDInsightScriptActionHistory</span><span class="sxs-lookup"><span data-stu-id="cd4c2-101">Get-AzureRmHDInsightScriptActionHistory</span></span>

## <span data-ttu-id="cd4c2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd4c2-103">Egy fürt parancsfájl-végrehajtási előzményeit jeleníti meg, és megfordítja őket fordított időrendi sorrendben, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd4c2-103">Gets the script action history for a cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd4c2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd4c2-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightScriptActionHistory [-ClusterName] <String> [[-ScriptExecutionId] <Int64>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd4c2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd4c2-105">DESCRIPTION</span></span>
<span data-ttu-id="cd4c2-106">A **Get-AzureRmHDInsightScriptActionHistory parancsmag beolvassa** az Azure HDInsight-fürtök parancsfájl-műveletek előzményeit, és a fordított időrendi sorrendben felsorolja azt, vagy egy korábban végrehajtott parancsfájl-művelet részleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd4c2-106">The **Get-AzureRmHDInsightScriptActionHistory** cmdlet gets the script action history for an Azure HDInsight cluster and lists it in reverse chronological order, or gets details of a previously executed script action.</span></span>

## <span data-ttu-id="cd4c2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cd4c2-107">EXAMPLES</span></span>

### <span data-ttu-id="cd4c2-108">Példa 1: egy fürt parancsfájl-végrehajtási műveleteinek előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd4c2-108">Example 1: Get the history of script actions executions for a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightScriptActionHistory -ClusterName "your-hadoop-001"
```

<span data-ttu-id="cd4c2-109">Ez a parancs a Hadoop-001-alapú fürthöz tartozó parancsfájl-műveletek előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cd4c2-109">This command gets the history of script actions for the cluster your-hadoop-001.</span></span>

## <span data-ttu-id="cd4c2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd4c2-110">PARAMETERS</span></span>

### <span data-ttu-id="cd4c2-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="cd4c2-111">-ClusterName</span></span>
<span data-ttu-id="cd4c2-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd4c2-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd4c2-113">-DefaultProfile</span></span>
<span data-ttu-id="cd4c2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cd4c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4c2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd4c2-115">-ResourceGroupName</span></span>
<span data-ttu-id="cd4c2-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd4c2-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4c2-117">-ScriptExecutionId</span><span class="sxs-lookup"><span data-stu-id="cd4c2-117">-ScriptExecutionId</span></span>
<span data-ttu-id="cd4c2-118">A futtatott parancsfájl műveleti AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="cd4c2-118">Specifies the execution ID of the executed script action.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd4c2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd4c2-119">CommonParameters</span></span>
<span data-ttu-id="cd4c2-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd4c2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd4c2-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd4c2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd4c2-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd4c2-122">INPUTS</span></span>

### <span data-ttu-id="cd4c2-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="cd4c2-123">None</span></span>
<span data-ttu-id="cd4c2-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cd4c2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd4c2-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd4c2-125">OUTPUTS</span></span>

### <span data-ttu-id="cd4c2-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptActionDetail]</span><span class="sxs-lookup"><span data-stu-id="cd4c2-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionDetail]</span></span>

## <span data-ttu-id="cd4c2-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd4c2-127">NOTES</span></span>

## <span data-ttu-id="cd4c2-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd4c2-128">RELATED LINKS</span></span>

