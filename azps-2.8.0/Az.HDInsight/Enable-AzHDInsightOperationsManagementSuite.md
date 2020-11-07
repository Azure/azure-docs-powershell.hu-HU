---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/enable-azhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Enable-AzHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c7d357df084a3843f8accbd3f54cc8aba9085012
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666369"
---
# <span data-ttu-id="d8a7c-101">Enable-AzHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="d8a7c-101">Enable-AzHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="d8a7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d8a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a7c-103">Engedélyezi a Operations Management Suite (OMS) HDInsight-fürtöt, és a megfelelő naplók az engedélyezés során megadott OMS-munkaterületre kerülnek.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

## <span data-ttu-id="d8a7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d8a7c-104">SYNTAX</span></span>

```
Enable-AzHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String> [-PrimaryKey] <String>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8a7c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d8a7c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a7c-106">Az **enable-AzHDInsightOperationsManagementSuite** parancsmag lehetővé teszi a Operations Management Suite (OMS) használatát az Azure HDInsight-fürtökben.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-106">The **Enable-AzHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d8a7c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d8a7c-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a7c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d8a7c-108">Example 1</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="d8a7c-109">A Operations Management Suite (OMS) engedélyezve lesz a HDInsight-fürtben, és a megfelelő naplók a OMS munkaterületre lesznek küldve azonosító 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="d8a7c-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="d8a7c-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="d8a7c-110">Example 2</span></span>
```
PS C:\> Enable-AzHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="d8a7c-111">A Operations Management Suite (OMS) engedélyezve lesz a HDInsight-fürtben, és a megfelelő naplók a OMS munkaterületre lesznek küldve azonosító 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="d8a7c-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="d8a7c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d8a7c-112">PARAMETERS</span></span>

### <span data-ttu-id="d8a7c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8a7c-113">-DefaultProfile</span></span>
<span data-ttu-id="d8a7c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d8a7c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8a7c-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d8a7c-115">-Name</span></span>
<span data-ttu-id="d8a7c-116">Annak a fürtnek a neve, amely engedélyezi a Operations Management Suite (OMS) használatát.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="d8a7c-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d8a7c-117">-PrimaryKey</span></span>
<span data-ttu-id="d8a7c-118">A Operations Management Suite (OMS) munkaterület elsődleges kulcsa.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a7c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8a7c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d8a7c-120">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="d8a7c-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d8a7c-121">-WorkspaceId</span></span>
<span data-ttu-id="d8a7c-122">A Operations Management Suite (OMS) munkaterület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8a7c-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d8a7c-123">-Confirm</span></span>
<span data-ttu-id="d8a7c-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8a7c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8a7c-125">-WhatIf</span></span>
<span data-ttu-id="d8a7c-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8a7c-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8a7c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8a7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a7c-128">CommonParameters</span></span>
<span data-ttu-id="d8a7c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d8a7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a7c-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a7c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a7c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8a7c-131">INPUTS</span></span>

### <span data-ttu-id="d8a7c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d8a7c-132">System.String</span></span>

## <span data-ttu-id="d8a7c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8a7c-133">OUTPUTS</span></span>

### <span data-ttu-id="d8a7c-134">Microsoft. Azure. Management. HDInsight. models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="d8a7c-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="d8a7c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d8a7c-135">NOTES</span></span>

## <span data-ttu-id="d8a7c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8a7c-136">RELATED LINKS</span></span>
