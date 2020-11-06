---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: f701d0c5e0ea2d8f4ce5ded850d131c6c066e9ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496159"
---
# <span data-ttu-id="63536-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="63536-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="63536-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="63536-102">SYNOPSIS</span></span>
<span data-ttu-id="63536-103">Letiltja a műveleti menedzsment programcsomagot (OMS) egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott OMS-munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="63536-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63536-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="63536-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63536-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="63536-105">DESCRIPTION</span></span>
<span data-ttu-id="63536-106">A **disable-AzureRmHDInsightOperationsManagementSuite** parancsmag letiltja a Operations Management Suite (OMS) alkalmazást az Azure HDInsight-fürtökben.</span><span class="sxs-lookup"><span data-stu-id="63536-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="63536-107">Példák</span><span class="sxs-lookup"><span data-stu-id="63536-107">EXAMPLES</span></span>

### <span data-ttu-id="63536-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="63536-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="63536-109">A Operations Management Suite (OMS) le lesz tiltva a HDInsight-fürtön, és a releváns naplók a OMS-munkaterületre való váltást követően megszűnnek.</span><span class="sxs-lookup"><span data-stu-id="63536-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="63536-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="63536-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="63536-111">A Operations Management Suite (OMS) le lesz tiltva a HDInsight-fürtön, és a releváns naplók a OMS-munkaterületre való váltást követően megszűnnek.</span><span class="sxs-lookup"><span data-stu-id="63536-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="63536-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="63536-112">PARAMETERS</span></span>

### <span data-ttu-id="63536-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63536-113">-DefaultProfile</span></span>
<span data-ttu-id="63536-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="63536-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63536-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="63536-115">-Name</span></span>
<span data-ttu-id="63536-116">Annak a fürtnek a neve, amely letiltja a Operations Management Suite (OMS) alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="63536-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="63536-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63536-117">-ResourceGroupName</span></span>
<span data-ttu-id="63536-118">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="63536-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="63536-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="63536-119">-Confirm</span></span>
<span data-ttu-id="63536-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="63536-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63536-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63536-121">-WhatIf</span></span>
<span data-ttu-id="63536-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="63536-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63536-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="63536-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63536-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63536-124">CommonParameters</span></span>
<span data-ttu-id="63536-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="63536-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63536-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63536-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63536-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="63536-127">INPUTS</span></span>

### <span data-ttu-id="63536-128">System. String</span><span class="sxs-lookup"><span data-stu-id="63536-128">System.String</span></span>

## <span data-ttu-id="63536-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="63536-129">OUTPUTS</span></span>

### <span data-ttu-id="63536-130">Microsoft. Azure. Management. HDInsight. models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="63536-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="63536-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="63536-131">NOTES</span></span>

## <span data-ttu-id="63536-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="63536-132">RELATED LINKS</span></span>
