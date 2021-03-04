---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 8ec48fe995d6f6be817d418714262706436ebf3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942386"
---
# <span data-ttu-id="df770-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="df770-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="df770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df770-102">SYNOPSIS</span></span>
<span data-ttu-id="df770-103">Leállítja az IIS-naplók számítógépekről való gyűjtését.</span><span class="sxs-lookup"><span data-stu-id="df770-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="df770-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="df770-104">SYNTAX</span></span>

### <span data-ttu-id="df770-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="df770-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df770-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="df770-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df770-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="df770-107">DESCRIPTION</span></span>
<span data-ttu-id="df770-108">A **Disable-AzOperationalInsightsIISLogCollection** parancsmag leállítja az IIS-naplóknak a munkaterületen csatlakoztatott számítógépekről való gyűjtését.</span><span class="sxs-lookup"><span data-stu-id="df770-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="df770-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="df770-109">EXAMPLES</span></span>

## <span data-ttu-id="df770-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df770-110">PARAMETERS</span></span>

### <span data-ttu-id="df770-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df770-111">-DefaultProfile</span></span>
<span data-ttu-id="df770-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="df770-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df770-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df770-113">-ResourceGroupName</span></span>
<span data-ttu-id="df770-114">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="df770-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="df770-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="df770-115">-Workspace</span></span>
<span data-ttu-id="df770-116">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="df770-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="df770-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="df770-117">-WorkspaceName</span></span>
<span data-ttu-id="df770-118">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="df770-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="df770-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df770-119">-Confirm</span></span>
<span data-ttu-id="df770-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="df770-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df770-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df770-121">-WhatIf</span></span>
<span data-ttu-id="df770-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="df770-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df770-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="df770-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df770-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df770-124">CommonParameters</span></span>
<span data-ttu-id="df770-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df770-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df770-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df770-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df770-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df770-127">INPUTS</span></span>

### <span data-ttu-id="df770-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="df770-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="df770-129">System.String</span><span class="sxs-lookup"><span data-stu-id="df770-129">System.String</span></span>

## <span data-ttu-id="df770-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="df770-130">OUTPUTS</span></span>

### <span data-ttu-id="df770-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="df770-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="df770-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="df770-132">NOTES</span></span>
* <span data-ttu-id="df770-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="df770-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="df770-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="df770-134">RELATED LINKS</span></span>

[<span data-ttu-id="df770-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="df770-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


