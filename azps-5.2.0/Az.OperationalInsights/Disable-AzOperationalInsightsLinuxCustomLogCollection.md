---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 94706768c6e5f222abe5a74ea32549f356abe1c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326658"
---
# <span data-ttu-id="d258d-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d258d-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="d258d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d258d-102">SYNOPSIS</span></span>
<span data-ttu-id="d258d-103">Leállítja az egyéni naplók linuxos számítógépekről való gyűjteményét.</span><span class="sxs-lookup"><span data-stu-id="d258d-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="d258d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d258d-104">SYNTAX</span></span>

### <span data-ttu-id="d258d-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d258d-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d258d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d258d-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d258d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d258d-107">DESCRIPTION</span></span>
<span data-ttu-id="d258d-108">A **Disable-AzOperationalInsightsLinuxCustomLogCollection** parancsmag leállítja az egyéni naplók gyűjteményét a csatlakoztatott Linux számítógépekről egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="d258d-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d258d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d258d-109">EXAMPLES</span></span>

## <span data-ttu-id="d258d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d258d-110">PARAMETERS</span></span>

### <span data-ttu-id="d258d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d258d-111">-DefaultProfile</span></span>
<span data-ttu-id="d258d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d258d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d258d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d258d-113">-ResourceGroupName</span></span>
<span data-ttu-id="d258d-114">Egy Linux rendszerű számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d258d-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d258d-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="d258d-115">-Workspace</span></span>
<span data-ttu-id="d258d-116">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d258d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d258d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d258d-117">-WorkspaceName</span></span>
<span data-ttu-id="d258d-118">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d258d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d258d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d258d-119">-Confirm</span></span>
<span data-ttu-id="d258d-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d258d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d258d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d258d-121">-WhatIf</span></span>
<span data-ttu-id="d258d-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d258d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d258d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d258d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d258d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d258d-124">CommonParameters</span></span>
<span data-ttu-id="d258d-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d258d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d258d-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d258d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d258d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d258d-127">INPUTS</span></span>

### <span data-ttu-id="d258d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d258d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d258d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d258d-129">System.String</span></span>

## <span data-ttu-id="d258d-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d258d-130">OUTPUTS</span></span>

### <span data-ttu-id="d258d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d258d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d258d-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d258d-132">NOTES</span></span>
* <span data-ttu-id="d258d-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="d258d-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d258d-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d258d-134">RELATED LINKS</span></span>

[<span data-ttu-id="d258d-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d258d-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


