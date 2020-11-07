---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: 01f9a2a9bae03606773c146f44f7e737fb9b613f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680544"
---
# <span data-ttu-id="f9446-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f9446-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="f9446-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f9446-102">SYNOPSIS</span></span>
<span data-ttu-id="f9446-103">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="f9446-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9446-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f9446-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9446-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f9446-105">DESCRIPTION</span></span>
<span data-ttu-id="f9446-106">A **use-AzureRmHDInsightCluster** parancsmag azt az Azure HDInsight-fürtöt adja meg, amely a kaptár-feladatok elvégzéséhez használható Invoke-AzureRmHDInsightHiveJob parancsmagot jelöli.</span><span class="sxs-lookup"><span data-stu-id="f9446-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="f9446-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f9446-107">EXAMPLES</span></span>

### <span data-ttu-id="f9446-108">1. példa: válasszon egy fürtöt a kaptár lekérdezések küldéséhez</span><span class="sxs-lookup"><span data-stu-id="f9446-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f9446-109">Ez a parancs kiválaszt egy fürtöt a kaptár-lekérdezések küldéséhez.</span><span class="sxs-lookup"><span data-stu-id="f9446-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="f9446-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f9446-110">PARAMETERS</span></span>

### <span data-ttu-id="f9446-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="f9446-111">-ClusterName</span></span>
<span data-ttu-id="f9446-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9446-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f9446-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f9446-113">-HttpCredential</span></span>
<span data-ttu-id="f9446-114">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="f9446-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="f9446-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9446-115">-ResourceGroupName</span></span>
<span data-ttu-id="f9446-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f9446-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f9446-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9446-117">-DefaultProfile</span></span>
<span data-ttu-id="f9446-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f9446-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9446-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9446-119">CommonParameters</span></span>
<span data-ttu-id="f9446-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f9446-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9446-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9446-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9446-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9446-122">INPUTS</span></span>

## <span data-ttu-id="f9446-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f9446-123">OUTPUTS</span></span>

### <span data-ttu-id="f9446-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f9446-124">System.String</span></span>

## <span data-ttu-id="f9446-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f9446-125">NOTES</span></span>

## <span data-ttu-id="f9446-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f9446-126">RELATED LINKS</span></span>

[<span data-ttu-id="f9446-127">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f9446-127">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="f9446-128">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f9446-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


