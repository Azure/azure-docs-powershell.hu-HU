---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/disable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Disable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 4f4508d38e4401198359fc816d1a94875f70940a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666375"
---
# <span data-ttu-id="d9427-101">Disable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="d9427-101">Disable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="d9427-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d9427-102">SYNOPSIS</span></span>
<span data-ttu-id="d9427-103">Letiltja a műveleti menedzsment programcsomagot (OMS) egy HDInsight-fürtben, és a releváns naplók az engedélyezés során meghatározott OMS-munkaterületre áramlanak.</span><span class="sxs-lookup"><span data-stu-id="d9427-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="d9427-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d9427-104">SYNTAX</span></span>

```
Disable-AzHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9427-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d9427-105">DESCRIPTION</span></span>
<span data-ttu-id="d9427-106">A **disable-AzHDInsightOperationsManagementSuite** parancsmag letiltja a Operations Management Suite (OMS) alkalmazást az Azure HDInsight-fürtökben.</span><span class="sxs-lookup"><span data-stu-id="d9427-106">The **Disable-AzHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d9427-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d9427-107">EXAMPLES</span></span>

### <span data-ttu-id="d9427-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d9427-108">Example 1</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="d9427-109">A Operations Management Suite (OMS) le lesz tiltva a HDInsight-fürtön, és a releváns naplók a OMS-munkaterületre való váltást követően megszűnnek.</span><span class="sxs-lookup"><span data-stu-id="d9427-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="d9427-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="d9427-110">Example 2</span></span>
```
PS C:\> Disable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="d9427-111">A Operations Management Suite (OMS) le lesz tiltva a HDInsight-fürtön, és a releváns naplók a OMS-munkaterületre való váltást követően megszűnnek.</span><span class="sxs-lookup"><span data-stu-id="d9427-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="d9427-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d9427-112">PARAMETERS</span></span>

### <span data-ttu-id="d9427-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9427-113">-DefaultProfile</span></span>
<span data-ttu-id="d9427-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d9427-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9427-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d9427-115">-Name</span></span>
<span data-ttu-id="d9427-116">Annak a fürtnek a neve, amely letiltja a Operations Management Suite (OMS) alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="d9427-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="d9427-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9427-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9427-118">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="d9427-118">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="d9427-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d9427-119">-Confirm</span></span>
<span data-ttu-id="d9427-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d9427-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9427-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9427-121">-WhatIf</span></span>
<span data-ttu-id="d9427-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d9427-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9427-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d9427-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9427-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9427-124">CommonParameters</span></span>
<span data-ttu-id="d9427-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d9427-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9427-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9427-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9427-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9427-127">INPUTS</span></span>

### <span data-ttu-id="d9427-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d9427-128">System.String</span></span>

## <span data-ttu-id="d9427-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d9427-129">OUTPUTS</span></span>

### <span data-ttu-id="d9427-130">Microsoft. Azure. Management. HDInsight. models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="d9427-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="d9427-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d9427-131">NOTES</span></span>

## <span data-ttu-id="d9427-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d9427-132">RELATED LINKS</span></span>
