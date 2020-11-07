---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/use-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: c8a58963e66c8260a0001c144230cabf3a80b295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680425"
---
# <span data-ttu-id="cefdf-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cefdf-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="cefdf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cefdf-102">SYNOPSIS</span></span>
<span data-ttu-id="cefdf-103">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="cefdf-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cefdf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cefdf-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cefdf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cefdf-105">DESCRIPTION</span></span>
<span data-ttu-id="cefdf-106">A **use-AzureRmHDInsightCluster** parancsmag azt az Azure HDInsight-fürtöt adja meg, amely a kaptár-feladatok elvégzéséhez használható Invoke-AzureRmHDInsightHiveJob parancsmagot jelöli.</span><span class="sxs-lookup"><span data-stu-id="cefdf-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="cefdf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cefdf-107">EXAMPLES</span></span>

### <span data-ttu-id="cefdf-108">1. példa: válasszon egy fürtöt a kaptár lekérdezések küldéséhez</span><span class="sxs-lookup"><span data-stu-id="cefdf-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="cefdf-109">Ez a parancs kiválaszt egy fürtöt a kaptár-lekérdezések küldéséhez.</span><span class="sxs-lookup"><span data-stu-id="cefdf-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="cefdf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cefdf-110">PARAMETERS</span></span>

### <span data-ttu-id="cefdf-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="cefdf-111">-ClusterName</span></span>
<span data-ttu-id="cefdf-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cefdf-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="cefdf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefdf-113">-DefaultProfile</span></span>
<span data-ttu-id="cefdf-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cefdf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cefdf-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="cefdf-115">-HttpCredential</span></span>
<span data-ttu-id="cefdf-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="cefdf-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cefdf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cefdf-117">-ResourceGroupName</span></span>
<span data-ttu-id="cefdf-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cefdf-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cefdf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefdf-119">CommonParameters</span></span>
<span data-ttu-id="cefdf-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cefdf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefdf-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cefdf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefdf-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cefdf-122">INPUTS</span></span>

### <span data-ttu-id="cefdf-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="cefdf-123">None</span></span>
<span data-ttu-id="cefdf-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="cefdf-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cefdf-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cefdf-125">OUTPUTS</span></span>

### <span data-ttu-id="cefdf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cefdf-126">System.String</span></span>

## <span data-ttu-id="cefdf-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cefdf-127">NOTES</span></span>

## <span data-ttu-id="cefdf-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cefdf-128">RELATED LINKS</span></span>

[<span data-ttu-id="cefdf-129">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cefdf-129">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="cefdf-130">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="cefdf-130">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


