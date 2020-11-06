---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 38c7bfe31faa8b4f167a14ede75f92055919ba55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505520"
---
# <span data-ttu-id="cef58-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="cef58-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="cef58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cef58-102">SYNOPSIS</span></span>
<span data-ttu-id="cef58-103">A OMS (Operations Management Suite) telepítésének állapotát kapja meg a fürtön.</span><span class="sxs-lookup"><span data-stu-id="cef58-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cef58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cef58-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cef58-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cef58-105">DESCRIPTION</span></span>
<span data-ttu-id="cef58-106">A **Get-AzureRmHDInsightOperationsManagementSuite** PARANCSMAG az OMS telepítésének állapotát egy Azure HDInsight-fürtben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cef58-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="cef58-107">Ha a OMS engedélyezve van, akkor a OMS munkaterület azonosítóját is visszaadja a program.</span><span class="sxs-lookup"><span data-stu-id="cef58-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="cef58-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cef58-108">EXAMPLES</span></span>

### <span data-ttu-id="cef58-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cef58-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="cef58-110">Az Operations Management Suite (OMS) engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="cef58-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="cef58-111">A OMS munkaterület-azonosító, ahol a naplók áramlanak 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="cef58-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="cef58-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="cef58-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="cef58-113">Az Operations Management Suite (OMS) engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="cef58-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="cef58-114">A OMS munkaterület-azonosító, ahol a naplók áramlanak 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="cef58-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="cef58-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="cef58-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="cef58-116">A Operations Management Suite (OMS) le van tiltva a fürtön, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="cef58-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="cef58-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="cef58-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="cef58-118">A Operations Management Suite (OMS) le van tiltva a fürtön, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="cef58-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="cef58-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cef58-119">PARAMETERS</span></span>

### <span data-ttu-id="cef58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef58-120">-DefaultProfile</span></span>
<span data-ttu-id="cef58-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cef58-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cef58-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cef58-122">-Name</span></span>
<span data-ttu-id="cef58-123">Annak a fürtnek a neve, amely a Operations Management Suite (OMS) állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cef58-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cef58-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef58-124">-ResourceGroupName</span></span>
<span data-ttu-id="cef58-125">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="cef58-125">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef58-126">CommonParameters</span></span>
<span data-ttu-id="cef58-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cef58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef58-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef58-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef58-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cef58-129">INPUTS</span></span>

### <span data-ttu-id="cef58-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cef58-130">System.String</span></span>

## <span data-ttu-id="cef58-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cef58-131">OUTPUTS</span></span>

### <span data-ttu-id="cef58-132">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cef58-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="cef58-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cef58-133">NOTES</span></span>

## <span data-ttu-id="cef58-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cef58-134">RELATED LINKS</span></span>

