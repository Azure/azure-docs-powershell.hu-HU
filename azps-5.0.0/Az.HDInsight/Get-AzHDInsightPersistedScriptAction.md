---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightPersistedScriptAction.md
ms.openlocfilehash: 56056e2933254401645a30e190a3a181b0c4514f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187842"
---
# <span data-ttu-id="b0114-101">Get-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0114-101">Get-AzHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="b0114-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b0114-102">SYNOPSIS</span></span>
<span data-ttu-id="b0114-103">Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="b0114-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="b0114-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b0114-104">SYNTAX</span></span>

```
Get-AzHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0114-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b0114-105">DESCRIPTION</span></span>
<span data-ttu-id="b0114-106">A **Get-AzHDInsightPersistedScriptAction parancsmag beolvassa** az Azure HDInsight-fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve részletezi a meghatározott állandó parancsfájl-műveletet.</span><span class="sxs-lookup"><span data-stu-id="b0114-106">The **Get-AzHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="b0114-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b0114-107">EXAMPLES</span></span>

### <span data-ttu-id="b0114-108">Példa 1: a kitartott parancsfájl-műveletek beszerzése egy fürtön</span><span class="sxs-lookup"><span data-stu-id="b0114-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b0114-109">Ez a parancs a Hadoop-001 nevű fürtben állandó parancsfájl-műveleteket kap.</span><span class="sxs-lookup"><span data-stu-id="b0114-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b0114-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b0114-110">PARAMETERS</span></span>

### <span data-ttu-id="b0114-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b0114-111">-ClusterName</span></span>
<span data-ttu-id="b0114-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0114-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b0114-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0114-113">-DefaultProfile</span></span>
<span data-ttu-id="b0114-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b0114-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0114-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b0114-115">-Name</span></span>
<span data-ttu-id="b0114-116">A fennálló parancsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0114-116">Specifies the name of the persisted script action.</span></span>

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

### <span data-ttu-id="b0114-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0114-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0114-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b0114-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b0114-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0114-119">CommonParameters</span></span>
<span data-ttu-id="b0114-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b0114-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0114-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0114-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0114-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0114-122">INPUTS</span></span>

### <span data-ttu-id="b0114-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b0114-123">None</span></span>

## <span data-ttu-id="b0114-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b0114-124">OUTPUTS</span></span>

### <span data-ttu-id="b0114-125">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightRuntimeScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0114-125">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction</span></span>

## <span data-ttu-id="b0114-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b0114-126">NOTES</span></span>

## <span data-ttu-id="b0114-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b0114-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0114-128">Remove-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0114-128">Remove-AzHDInsightPersistedScriptAction</span></span>](./Remove-AzHDInsightPersistedScriptAction.md)

[<span data-ttu-id="b0114-129">Set-AzHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="b0114-129">Set-AzHDInsightPersistedScriptAction</span></span>](./Set-AzHDInsightPersistedScriptAction.md)

