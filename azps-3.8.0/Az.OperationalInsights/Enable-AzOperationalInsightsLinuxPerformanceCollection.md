---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 3a914aa970282d5157c9c72de0e328d7b927a238
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93844954"
---
# <span data-ttu-id="a7ddc-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="a7ddc-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="a7ddc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="a7ddc-103">Elindítja a teljesítményszámlálók gyűjteményét a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="a7ddc-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="a7ddc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7ddc-104">SYNTAX</span></span>

### <span data-ttu-id="a7ddc-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7ddc-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7ddc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a7ddc-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7ddc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7ddc-107">DESCRIPTION</span></span>
<span data-ttu-id="a7ddc-108">Az **enable-AzOperationalInsightsLinuxPerformanceCollection** parancsmag a csatlakoztatott linuxos számítógépekről származó teljesítményszámlálók gyűjteményét indítja el egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="a7ddc-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="a7ddc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a7ddc-109">EXAMPLES</span></span>

## <span data-ttu-id="a7ddc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7ddc-110">PARAMETERS</span></span>

### <span data-ttu-id="a7ddc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7ddc-111">-DefaultProfile</span></span>
<span data-ttu-id="a7ddc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a7ddc-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7ddc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7ddc-113">-ResourceGroupName</span></span>
<span data-ttu-id="a7ddc-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7ddc-114">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ddc-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="a7ddc-115">-Workspace</span></span>
<span data-ttu-id="a7ddc-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="a7ddc-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ddc-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a7ddc-117">-WorkspaceName</span></span>
<span data-ttu-id="a7ddc-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="a7ddc-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7ddc-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a7ddc-119">-Confirm</span></span>
<span data-ttu-id="a7ddc-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a7ddc-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ddc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7ddc-121">-WhatIf</span></span>
<span data-ttu-id="a7ddc-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a7ddc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7ddc-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7ddc-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7ddc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7ddc-124">CommonParameters</span></span>
<span data-ttu-id="a7ddc-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7ddc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7ddc-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7ddc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7ddc-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7ddc-127">INPUTS</span></span>

### <span data-ttu-id="a7ddc-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a7ddc-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="a7ddc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a7ddc-129">System.String</span></span>

## <span data-ttu-id="a7ddc-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7ddc-130">OUTPUTS</span></span>

### <span data-ttu-id="a7ddc-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="a7ddc-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="a7ddc-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7ddc-132">NOTES</span></span>
* <span data-ttu-id="a7ddc-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="a7ddc-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="a7ddc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7ddc-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7ddc-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="a7ddc-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


