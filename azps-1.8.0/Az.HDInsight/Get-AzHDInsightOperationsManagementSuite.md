---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fa19e7817d9d9be5e0c941db6d814500bad33509
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836053"
---
# <span data-ttu-id="dfa20-101">Get-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="dfa20-101">Get-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="dfa20-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfa20-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa20-103">A OMS (Operations Management Suite) telepítésének állapotát kapja meg a fürtön.</span><span class="sxs-lookup"><span data-stu-id="dfa20-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

## <span data-ttu-id="dfa20-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfa20-104">SYNTAX</span></span>

```
Get-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfa20-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfa20-105">DESCRIPTION</span></span>
<span data-ttu-id="dfa20-106">A **Get-AzHDInsightOperationsManagementSuite** PARANCSMAG az OMS telepítésének állapotát egy Azure HDInsight-fürtben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dfa20-106">The **Get-AzHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="dfa20-107">Ha a OMS engedélyezve van, akkor a OMS munkaterület azonosítóját is visszaadja a program.</span><span class="sxs-lookup"><span data-stu-id="dfa20-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="dfa20-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dfa20-108">EXAMPLES</span></span>

### <span data-ttu-id="dfa20-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="dfa20-109">Example 1</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="dfa20-110">Az Operations Management Suite (OMS) engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="dfa20-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="dfa20-111">A OMS munkaterület-azonosító, ahol a naplók áramlanak 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="dfa20-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="dfa20-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="dfa20-112">Example 2</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="dfa20-113">Az Operations Management Suite (OMS) engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="dfa20-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="dfa20-114">A OMS munkaterület-azonosító, ahol a naplók áramlanak 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="dfa20-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="dfa20-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="dfa20-115">Example 3</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="dfa20-116">A Operations Management Suite (OMS) le van tiltva a fürtön, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="dfa20-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="dfa20-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="dfa20-117">Example 4</span></span>
```
PS C:\> Get-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="dfa20-118">A Operations Management Suite (OMS) le van tiltva a fürtön, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="dfa20-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="dfa20-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfa20-119">PARAMETERS</span></span>

### <span data-ttu-id="dfa20-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa20-120">-DefaultProfile</span></span>
<span data-ttu-id="dfa20-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="dfa20-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfa20-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dfa20-122">-Name</span></span>
<span data-ttu-id="dfa20-123">Annak a fürtnek a neve, amely a Operations Management Suite (OMS) állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dfa20-123">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfa20-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfa20-125">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="dfa20-125">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfa20-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa20-126">CommonParameters</span></span>
<span data-ttu-id="dfa20-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfa20-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa20-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfa20-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa20-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfa20-129">INPUTS</span></span>

### <span data-ttu-id="dfa20-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dfa20-130">System.String</span></span>

## <span data-ttu-id="dfa20-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfa20-131">OUTPUTS</span></span>

### <span data-ttu-id="dfa20-132">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="dfa20-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="dfa20-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfa20-133">NOTES</span></span>

## <span data-ttu-id="dfa20-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfa20-134">RELATED LINKS</span></span>
