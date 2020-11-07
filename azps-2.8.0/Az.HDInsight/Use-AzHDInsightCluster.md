---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 7e9df747becd5e2bd49b865b61f963d1db585e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666322"
---
# <span data-ttu-id="d7bfe-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d7bfe-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="d7bfe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bfe-103">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="d7bfe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7bfe-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7bfe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="d7bfe-106">A **use-AzHDInsightCluster** parancsmag azt az Azure HDInsight-fürtöt adja meg, amely a kaptár-feladatok elvégzéséhez használható Invoke-AzHDInsightHiveJob parancsmagot jelöli.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="d7bfe-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d7bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="d7bfe-108">1. példa: válasszon egy fürtöt a kaptár lekérdezések küldéséhez</span><span class="sxs-lookup"><span data-stu-id="d7bfe-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="d7bfe-109">Ez a parancs kiválaszt egy fürtöt a kaptár-lekérdezések küldéséhez.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="d7bfe-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7bfe-110">PARAMETERS</span></span>

### <span data-ttu-id="d7bfe-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="d7bfe-111">-ClusterName</span></span>
<span data-ttu-id="d7bfe-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d7bfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bfe-113">-DefaultProfile</span></span>
<span data-ttu-id="d7bfe-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d7bfe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7bfe-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d7bfe-115">-HttpCredential</span></span>
<span data-ttu-id="d7bfe-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bfe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bfe-117">-ResourceGroupName</span></span>
<span data-ttu-id="d7bfe-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7bfe-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d7bfe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bfe-119">CommonParameters</span></span>
<span data-ttu-id="d7bfe-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7bfe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bfe-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bfe-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bfe-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7bfe-122">INPUTS</span></span>

### <span data-ttu-id="d7bfe-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7bfe-123">None</span></span>

## <span data-ttu-id="d7bfe-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7bfe-124">OUTPUTS</span></span>

### <span data-ttu-id="d7bfe-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d7bfe-125">System.String</span></span>

## <span data-ttu-id="d7bfe-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7bfe-126">NOTES</span></span>

## <span data-ttu-id="d7bfe-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7bfe-127">RELATED LINKS</span></span>

[<span data-ttu-id="d7bfe-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d7bfe-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="d7bfe-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d7bfe-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


