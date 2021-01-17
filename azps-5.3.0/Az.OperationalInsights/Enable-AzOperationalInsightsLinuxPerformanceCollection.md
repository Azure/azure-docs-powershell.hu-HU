---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 3a914aa970282d5157c9c72de0e328d7b927a238
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481089"
---
# <span data-ttu-id="7f556-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="7f556-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="7f556-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f556-102">SYNOPSIS</span></span>
<span data-ttu-id="7f556-103">Elindítja a teljesítményszámlálók gyűjteményét Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="7f556-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="7f556-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7f556-104">SYNTAX</span></span>

### <span data-ttu-id="7f556-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7f556-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f556-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7f556-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f556-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7f556-107">DESCRIPTION</span></span>
<span data-ttu-id="7f556-108">Az **Enable-AzOperationalInsightsLinuxPerformanceCollection parancsmag** elindítja a teljesítmény-számlálók gyűjteményét a csatlakoztatott Linux számítógépekről egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="7f556-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="7f556-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7f556-109">EXAMPLES</span></span>

## <span data-ttu-id="7f556-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f556-110">PARAMETERS</span></span>

### <span data-ttu-id="7f556-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f556-111">-DefaultProfile</span></span>
<span data-ttu-id="7f556-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7f556-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f556-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f556-113">-ResourceGroupName</span></span>
<span data-ttu-id="7f556-114">Egy Linux rendszerű számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7f556-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="7f556-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="7f556-115">-Workspace</span></span>
<span data-ttu-id="7f556-116">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="7f556-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7f556-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7f556-117">-WorkspaceName</span></span>
<span data-ttu-id="7f556-118">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="7f556-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7f556-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f556-119">-Confirm</span></span>
<span data-ttu-id="7f556-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7f556-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f556-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f556-121">-WhatIf</span></span>
<span data-ttu-id="7f556-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7f556-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f556-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7f556-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f556-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f556-124">CommonParameters</span></span>
<span data-ttu-id="7f556-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f556-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f556-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f556-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f556-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f556-127">INPUTS</span></span>

### <span data-ttu-id="7f556-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7f556-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7f556-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7f556-129">System.String</span></span>

## <span data-ttu-id="7f556-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7f556-130">OUTPUTS</span></span>

### <span data-ttu-id="7f556-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7f556-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7f556-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7f556-132">NOTES</span></span>
* <span data-ttu-id="7f556-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="7f556-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="7f556-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7f556-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f556-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="7f556-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


