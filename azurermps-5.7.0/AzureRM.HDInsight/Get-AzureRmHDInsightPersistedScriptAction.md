---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2B7C1B83-EEEA-4BD1-9E9B-1F3070295995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightpersistedscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightPersistedScriptAction.md
ms.openlocfilehash: c70b4fecc9be5937d24ca4bc84b8aa6554daf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505519"
---
# <span data-ttu-id="87b68-101">Get-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="87b68-101">Get-AzureRmHDInsightPersistedScriptAction</span></span>

## <span data-ttu-id="87b68-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87b68-102">SYNOPSIS</span></span>
<span data-ttu-id="87b68-103">Beolvassa a fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve a megadott, kimaradt parancsfájlokra vonatkozó adatokat kap.</span><span class="sxs-lookup"><span data-stu-id="87b68-103">Gets the persisted script actions for a cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87b68-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87b68-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightPersistedScriptAction [-ClusterName] <String> [[-Name] <String>]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87b68-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87b68-105">DESCRIPTION</span></span>
<span data-ttu-id="87b68-106">A **Get-AzureRmHDInsightPersistedScriptAction parancsmag beolvassa** az Azure HDInsight-fürtök állandó parancsfájlokkal kapcsolatos műveleteit, és időrendi sorrendben listázza őket, illetve részletezi a meghatározott állandó parancsfájl-műveletet.</span><span class="sxs-lookup"><span data-stu-id="87b68-106">The **Get-AzureRmHDInsightPersistedScriptAction** cmdlet gets the persisted script actions for an Azure HDInsight cluster and lists them in chronological order, or gets details for a specified persisted script action.</span></span>

## <span data-ttu-id="87b68-107">Példák</span><span class="sxs-lookup"><span data-stu-id="87b68-107">EXAMPLES</span></span>

### <span data-ttu-id="87b68-108">Példa 1: a kitartott parancsfájl-műveletek beszerzése egy fürtön</span><span class="sxs-lookup"><span data-stu-id="87b68-108">Example 1: Get the persisted script actions on a cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightPersistedScriptAction -ClusterName "your-hadoop-001"
```

<span data-ttu-id="87b68-109">Ez a parancs a Hadoop-001 nevű fürtben állandó parancsfájl-műveleteket kap.</span><span class="sxs-lookup"><span data-stu-id="87b68-109">This command gets persisted script actions on the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="87b68-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87b68-110">PARAMETERS</span></span>

### <span data-ttu-id="87b68-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="87b68-111">-ClusterName</span></span>
<span data-ttu-id="87b68-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87b68-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="87b68-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b68-113">-DefaultProfile</span></span>
<span data-ttu-id="87b68-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="87b68-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87b68-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87b68-115">-Name</span></span>
<span data-ttu-id="87b68-116">A fennálló parancsfájl nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87b68-116">Specifies the name of the persisted script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87b68-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87b68-117">-ResourceGroupName</span></span>
<span data-ttu-id="87b68-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87b68-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="87b68-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b68-119">CommonParameters</span></span>
<span data-ttu-id="87b68-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87b68-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b68-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87b68-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b68-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87b68-122">INPUTS</span></span>

### <span data-ttu-id="87b68-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="87b68-123">None</span></span>
<span data-ttu-id="87b68-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="87b68-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87b68-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87b68-125">OUTPUTS</span></span>

### <span data-ttu-id="87b68-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. commands. HDInsight. models. Management. AzureHDInsightRuntimeScriptAction]</span><span class="sxs-lookup"><span data-stu-id="87b68-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptAction]</span></span>

## <span data-ttu-id="87b68-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87b68-127">NOTES</span></span>

## <span data-ttu-id="87b68-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87b68-128">RELATED LINKS</span></span>

[<span data-ttu-id="87b68-129">Remove-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="87b68-129">Remove-AzureRmHDInsightPersistedScriptAction</span></span>](./Remove-AzureRmHDInsightPersistedScriptAction.md)

[<span data-ttu-id="87b68-130">Set-AzureRmHDInsightPersistedScriptAction</span><span class="sxs-lookup"><span data-stu-id="87b68-130">Set-AzureRmHDInsightPersistedScriptAction</span></span>](./Set-AzureRmHDInsightPersistedScriptAction.md)

