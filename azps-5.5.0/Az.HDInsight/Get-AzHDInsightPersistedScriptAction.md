---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: b5d62e963bdd2f30ab0c5b821854ee46b391376b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207343"
---
# <span data-ttu-id="e1e64-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e1e64-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="e1e64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1e64-102">SYNOPSIS</span></span>
<span data-ttu-id="e1e64-103">Lejátsa egy fürt megőrzött parancsprogram-műveletét, és időrendben felsorolja őket, vagy egy adott állandó parancsfájlművelet részleteit.</span><span class="sxs-lookup"><span data-stu-id="e1e64-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="e1e64-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e1e64-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1e64-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e1e64-105">DESCRIPTION</span></span>
<span data-ttu-id="e1e64-106">A **Get-AzHDInsightPersistedScriptAction parancsmag** az Azure HDInsight-fürt állandó parancsfájlműveleteit kapja meg, és időrendben listázza őket, vagy egy megadott állandó parancsfájlművelet részleteit is megjeleníti.</span><span class="sxs-lookup"><span data-stu-id="e1e64-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="e1e64-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e1e64-107">EXAMPLES</span></span>

### <span data-ttu-id="e1e64-108">1. példa: Az állandó parancsfájl-műveletek lekérte egy fürtön</span><span class="sxs-lookup"><span data-stu-id="e1e64-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="e1e64-109">Ez a parancs megőrzetlen parancsműveleteket kap a -hadoop-001 nevű fürtben.</span><span class="sxs-lookup"><span data-stu-id="e1e64-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e1e64-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1e64-110">PARAMETERS</span></span>

### <span data-ttu-id="e1e64-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e1e64-111">-ClusterName</span></span>
<span data-ttu-id="e1e64-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1e64-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e1e64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1e64-113">-DefaultProfile</span></span>
<span data-ttu-id="e1e64-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e1e64-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1e64-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e1e64-115">-Name</span></span>
<span data-ttu-id="e1e64-116">Az állandó parancsfájl-művelet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1e64-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1e64-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1e64-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1e64-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e1e64-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e1e64-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1e64-119">CommonParameters</span></span>
<span data-ttu-id="e1e64-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1e64-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1e64-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e1e64-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1e64-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e1e64-122">INPUTS</span></span>

### <span data-ttu-id="e1e64-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="e1e64-123">None</span></span>

## <span data-ttu-id="e1e64-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e1e64-124">OUTPUTS</span></span>

### <span data-ttu-id="e1e64-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="e1e64-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="e1e64-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e1e64-126">NOTES</span></span>

## <span data-ttu-id="e1e64-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e1e64-127">RELATED LINKS</span></span>

[<span data-ttu-id="e1e64-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e1e64-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="e1e64-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="e1e64-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)


