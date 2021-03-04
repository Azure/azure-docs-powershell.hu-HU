---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 16aabb8fe12569c6c230248fcea8038e1a162f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942337"
---
# <span data-ttu-id="9fdb0-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="9fdb0-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="9fdb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fdb0-102">SYNOPSIS</span></span>
<span data-ttu-id="9fdb0-103">Egyéni naplók gyűjteményét kezdi Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="9fdb0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9fdb0-104">SYNTAX</span></span>

### <span data-ttu-id="9fdb0-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fdb0-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdb0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9fdb0-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fdb0-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9fdb0-107">DESCRIPTION</span></span>
<span data-ttu-id="9fdb0-108">Az **Enable-AzOperationalInsightsLinuxCustomLogCollection** parancsmag elindítja az egyéni naplók gyűjteményét a csatlakoztatott Linux számítógépekről egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="9fdb0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9fdb0-109">EXAMPLES</span></span>

## <span data-ttu-id="9fdb0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fdb0-110">PARAMETERS</span></span>

### <span data-ttu-id="9fdb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fdb0-111">-DefaultProfile</span></span>
<span data-ttu-id="9fdb0-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9fdb0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fdb0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fdb0-113">-ResourceGroupName</span></span>
<span data-ttu-id="9fdb0-114">Egy Linux rendszerű számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="9fdb0-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="9fdb0-115">-Workspace</span></span>
<span data-ttu-id="9fdb0-116">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9fdb0-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9fdb0-117">-WorkspaceName</span></span>
<span data-ttu-id="9fdb0-118">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9fdb0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fdb0-119">-Confirm</span></span>
<span data-ttu-id="9fdb0-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fdb0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fdb0-121">-WhatIf</span></span>
<span data-ttu-id="9fdb0-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fdb0-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fdb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fdb0-124">CommonParameters</span></span>
<span data-ttu-id="9fdb0-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fdb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fdb0-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fdb0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fdb0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fdb0-127">INPUTS</span></span>

### <span data-ttu-id="9fdb0-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9fdb0-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9fdb0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9fdb0-129">System.String</span></span>

## <span data-ttu-id="9fdb0-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fdb0-130">OUTPUTS</span></span>

### <span data-ttu-id="9fdb0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9fdb0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9fdb0-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9fdb0-132">NOTES</span></span>
* <span data-ttu-id="9fdb0-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="9fdb0-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9fdb0-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fdb0-134">RELATED LINKS</span></span>

[<span data-ttu-id="9fdb0-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="9fdb0-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


