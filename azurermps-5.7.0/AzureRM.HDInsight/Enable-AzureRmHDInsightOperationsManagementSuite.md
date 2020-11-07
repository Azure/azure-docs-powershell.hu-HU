---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/enable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 33d06939ad9c3f76bac5ae04124236656991c842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672861"
---
# <span data-ttu-id="659d4-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="659d4-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="659d4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="659d4-102">SYNOPSIS</span></span>
<span data-ttu-id="659d4-103">Engedélyezi a Operations Management Suite (OMS) HDInsight-fürtöt, és a megfelelő naplók az engedélyezés során megadott OMS-munkaterületre kerülnek.</span><span class="sxs-lookup"><span data-stu-id="659d4-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="659d4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="659d4-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="659d4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="659d4-105">DESCRIPTION</span></span>
<span data-ttu-id="659d4-106">Az **enable-AzureRmHDInsightOperationsManagementSuite** parancsmag lehetővé teszi a Operations Management Suite (OMS) használatát az Azure HDInsight-fürtökben.</span><span class="sxs-lookup"><span data-stu-id="659d4-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="659d4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="659d4-107">EXAMPLES</span></span>

### <span data-ttu-id="659d4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="659d4-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="659d4-109">A Operations Management Suite (OMS) engedélyezve lesz a HDInsight-fürtben, és a megfelelő naplók a OMS munkaterületre lesznek küldve azonosító 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="659d4-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="659d4-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="659d4-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="659d4-111">A Operations Management Suite (OMS) engedélyezve lesz a HDInsight-fürtben, és a megfelelő naplók a OMS munkaterületre lesznek küldve azonosító 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="659d4-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="659d4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="659d4-112">PARAMETERS</span></span>

### <span data-ttu-id="659d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="659d4-113">-DefaultProfile</span></span>
<span data-ttu-id="659d4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="659d4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="659d4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="659d4-115">-Name</span></span>
<span data-ttu-id="659d4-116">Annak a fürtnek a neve, amely engedélyezi a Operations Management Suite (OMS) használatát.</span><span class="sxs-lookup"><span data-stu-id="659d4-116">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

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

### <span data-ttu-id="659d4-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="659d4-117">-PrimaryKey</span></span>
<span data-ttu-id="659d4-118">A Operations Management Suite (OMS) munkaterület elsődleges kulcsa.</span><span class="sxs-lookup"><span data-stu-id="659d4-118">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="659d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="659d4-120">A fürt erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="659d4-120">The resource group of the cluster.</span></span>

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

### <span data-ttu-id="659d4-121">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="659d4-121">-WorkspaceId</span></span>
<span data-ttu-id="659d4-122">A Operations Management Suite (OMS) munkaterület azonosítója.</span><span class="sxs-lookup"><span data-stu-id="659d4-122">The id of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659d4-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="659d4-123">-Confirm</span></span>
<span data-ttu-id="659d4-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="659d4-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659d4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="659d4-125">-WhatIf</span></span>
<span data-ttu-id="659d4-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="659d4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="659d4-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="659d4-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="659d4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="659d4-128">CommonParameters</span></span>
<span data-ttu-id="659d4-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="659d4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="659d4-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="659d4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="659d4-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="659d4-131">INPUTS</span></span>

### <span data-ttu-id="659d4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="659d4-132">System.String</span></span>

## <span data-ttu-id="659d4-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="659d4-133">OUTPUTS</span></span>

### <span data-ttu-id="659d4-134">Microsoft. Azure. Management. HDInsight. models. OperationResource</span><span class="sxs-lookup"><span data-stu-id="659d4-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="659d4-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="659d4-135">NOTES</span></span>

## <span data-ttu-id="659d4-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="659d4-136">RELATED LINKS</span></span>

