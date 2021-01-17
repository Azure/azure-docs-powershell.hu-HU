---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468813"
---
# <span data-ttu-id="d0a60-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="d0a60-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="d0a60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0a60-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a60-103">Egyéni naplózási házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="d0a60-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="d0a60-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d0a60-104">SYNTAX</span></span>

### <span data-ttu-id="d0a60-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0a60-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0a60-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d0a60-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0a60-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d0a60-107">DESCRIPTION</span></span>
<span data-ttu-id="d0a60-108">A **New-AzOperationalInsightsCustomLogDataSource** parancsmag egyéni naplózási házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="d0a60-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="d0a60-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d0a60-109">EXAMPLES</span></span>

## <span data-ttu-id="d0a60-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0a60-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a60-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="d0a60-111">-CustomLogRawJson</span></span>
<span data-ttu-id="d0a60-112">Az egyéni gyűjtemény házirendet nyers JavaScript-objektum-notation (JSON) karakterláncként adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0a60-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a60-113">-DefaultProfile</span></span>
<span data-ttu-id="d0a60-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d0a60-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0a60-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d0a60-115">-Force</span></span>
<span data-ttu-id="d0a60-116">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="d0a60-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a60-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d0a60-117">-Name</span></span>
<span data-ttu-id="d0a60-118">Megadja az adatforrás nevét.</span><span class="sxs-lookup"><span data-stu-id="d0a60-118">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a60-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a60-119">-ResourceGroupName</span></span>
<span data-ttu-id="d0a60-120">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0a60-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="d0a60-121">-Workspace</span><span class="sxs-lookup"><span data-stu-id="d0a60-121">-Workspace</span></span>
<span data-ttu-id="d0a60-122">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d0a60-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d0a60-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d0a60-123">-WorkspaceName</span></span>
<span data-ttu-id="d0a60-124">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d0a60-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d0a60-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0a60-125">-Confirm</span></span>
<span data-ttu-id="d0a60-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d0a60-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a60-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a60-127">-WhatIf</span></span>
<span data-ttu-id="d0a60-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d0a60-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a60-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d0a60-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a60-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a60-130">CommonParameters</span></span>
<span data-ttu-id="d0a60-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a60-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a60-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a60-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a60-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0a60-133">INPUTS</span></span>

### <span data-ttu-id="d0a60-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0a60-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d0a60-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d0a60-135">System.String</span></span>

## <span data-ttu-id="d0a60-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0a60-136">OUTPUTS</span></span>

### <span data-ttu-id="d0a60-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d0a60-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d0a60-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d0a60-138">NOTES</span></span>

## <span data-ttu-id="d0a60-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0a60-139">RELATED LINKS</span></span>

[<span data-ttu-id="d0a60-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d0a60-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="d0a60-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d0a60-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


