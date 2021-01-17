---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: f48007be3e1209cff65e46c669bce46298182247
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384927"
---
# <span data-ttu-id="10fe7-101">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="10fe7-101">Enable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="10fe7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="10fe7-103">Elindítja az IIS-naplók gyűjteményét egy munkaterület számítógépein.</span><span class="sxs-lookup"><span data-stu-id="10fe7-103">Starts collection of IIS logs from computers in a workspace.</span></span>

## <span data-ttu-id="10fe7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="10fe7-104">SYNTAX</span></span>

### <span data-ttu-id="10fe7-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10fe7-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10fe7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="10fe7-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10fe7-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="10fe7-107">DESCRIPTION</span></span>
<span data-ttu-id="10fe7-108">Az **Enable-AzOperationalInsightsIISLogCollection** parancsmag elindítja az IIS-naplók gyűjteményét egy munkaterület csatlakoztatott számítógépein.</span><span class="sxs-lookup"><span data-stu-id="10fe7-108">The **Enable-AzOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="10fe7-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="10fe7-109">EXAMPLES</span></span>

## <span data-ttu-id="10fe7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10fe7-110">PARAMETERS</span></span>

### <span data-ttu-id="10fe7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10fe7-111">-DefaultProfile</span></span>
<span data-ttu-id="10fe7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="10fe7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10fe7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10fe7-113">-ResourceGroupName</span></span>
<span data-ttu-id="10fe7-114">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="10fe7-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="10fe7-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="10fe7-115">-Workspace</span></span>
<span data-ttu-id="10fe7-116">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="10fe7-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="10fe7-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="10fe7-117">-WorkspaceName</span></span>
<span data-ttu-id="10fe7-118">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="10fe7-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="10fe7-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10fe7-119">-Confirm</span></span>
<span data-ttu-id="10fe7-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="10fe7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10fe7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10fe7-121">-WhatIf</span></span>
<span data-ttu-id="10fe7-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="10fe7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10fe7-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="10fe7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10fe7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10fe7-124">CommonParameters</span></span>
<span data-ttu-id="10fe7-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10fe7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10fe7-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10fe7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10fe7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10fe7-127">INPUTS</span></span>

### <span data-ttu-id="10fe7-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="10fe7-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="10fe7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="10fe7-129">System.String</span></span>

## <span data-ttu-id="10fe7-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10fe7-130">OUTPUTS</span></span>

### <span data-ttu-id="10fe7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="10fe7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="10fe7-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="10fe7-132">NOTES</span></span>

## <span data-ttu-id="10fe7-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10fe7-133">RELATED LINKS</span></span>

[<span data-ttu-id="10fe7-134">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="10fe7-134">Disable-AzOperationalInsightsIISLogCollection</span></span>](./Disable-AzOperationalInsightsIISLogCollection.md)


