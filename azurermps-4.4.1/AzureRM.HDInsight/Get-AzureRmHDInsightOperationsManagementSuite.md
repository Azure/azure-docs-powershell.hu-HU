---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 0f3e9e542ff1d05a9872096a784c8dabfed1910b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680560"
---
# <span data-ttu-id="3d10c-101">Get-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="3d10c-101">Get-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="3d10c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d10c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d10c-103">A OMS (Operations Management Suite) telepítésének állapotát kapja meg a fürtön.</span><span class="sxs-lookup"><span data-stu-id="3d10c-103">Gets the status of Operations Management Suite (OMS) installation on the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d10c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d10c-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d10c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d10c-105">DESCRIPTION</span></span>
<span data-ttu-id="3d10c-106">A **Get-AzureRmHDInsightOperationsManagementSuite** PARANCSMAG az OMS telepítésének állapotát egy Azure HDInsight-fürtben kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3d10c-106">The **Get-AzureRmHDInsightOperationsManagementSuite** cmdlet gets the status of OMS installation in an Azure HDInsight cluster.</span></span> <span data-ttu-id="3d10c-107">Ha a OMS engedélyezve van, akkor a OMS munkaterület azonosítóját is visszaadja a program.</span><span class="sxs-lookup"><span data-stu-id="3d10c-107">If OMS is enabled then it will also return the OMS workspace id.</span></span>

## <span data-ttu-id="3d10c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3d10c-108">EXAMPLES</span></span>

### <span data-ttu-id="3d10c-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3d10c-109">Example 1</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="3d10c-110">Az Operations Management Suite (OMS) engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="3d10c-110">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="3d10c-111">A OMS munkaterület-azonosító, ahol a naplók áramlanak 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="3d10c-111">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="3d10c-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="3d10c-112">Example 2</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

<span data-ttu-id="3d10c-113">Az Operations Management Suite (OMS) engedélyezve van a fürtön, mert a ClusterMonitoringEnabled tulajdonság igaz.</span><span class="sxs-lookup"><span data-stu-id="3d10c-113">Operations Management Suite (OMS) is enabled on the cluster because the ClusterMonitoringEnabled property is true.</span></span> <span data-ttu-id="3d10c-114">A OMS munkaterület-azonosító, ahol a naplók áramlanak 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="3d10c-114">The OMS workspace id where the logs are flowing is 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="3d10c-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="3d10c-115">Example 3</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="3d10c-116">A Operations Management Suite (OMS) le van tiltva a fürtön, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="3d10c-116">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

### <span data-ttu-id="3d10c-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="3d10c-117">Example 4</span></span>
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

<span data-ttu-id="3d10c-118">A Operations Management Suite (OMS) le van tiltva a fürtön, mert a ClusterMonitoringEnabled tulajdonság hamis.</span><span class="sxs-lookup"><span data-stu-id="3d10c-118">Operations Management Suite (OMS) is disabled on the cluster because the ClusterMonitoringEnabled property is false.</span></span>

## <span data-ttu-id="3d10c-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d10c-119">PARAMETERS</span></span>

### <span data-ttu-id="3d10c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d10c-120">-Name</span></span>
<span data-ttu-id="3d10c-121">Annak a fürtnek a neve, amely a Operations Management Suite (OMS) állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3d10c-121">The name of the cluster to get the status of Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="3d10c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d10c-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d10c-123">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="3d10c-123">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="3d10c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d10c-124">-DefaultProfile</span></span>
<span data-ttu-id="3d10c-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d10c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d10c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d10c-126">CommonParameters</span></span>
<span data-ttu-id="3d10c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d10c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d10c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d10c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d10c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d10c-129">INPUTS</span></span>

### <span data-ttu-id="3d10c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3d10c-130">System.String</span></span>

## <span data-ttu-id="3d10c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d10c-131">OUTPUTS</span></span>

### <span data-ttu-id="3d10c-132">Microsoft. Azure. Command. HDInsight. models. Management. AzureHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="3d10c-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightOMS</span></span>

## <span data-ttu-id="3d10c-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d10c-133">NOTES</span></span>

## <span data-ttu-id="3d10c-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d10c-134">RELATED LINKS</span></span>

