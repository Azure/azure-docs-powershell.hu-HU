---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187231"
---
# <span data-ttu-id="c2cf6-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="c2cf6-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="c2cf6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="c2cf6-103">Egyéni naplózási házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="c2cf6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2cf6-104">SYNTAX</span></span>

### <span data-ttu-id="c2cf6-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2cf6-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2cf6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c2cf6-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2cf6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2cf6-107">DESCRIPTION</span></span>
<span data-ttu-id="c2cf6-108">A **New-AzOperationalInsightsCustomLogDataSource** parancsmag egyéni naplózási házirendet határoz meg.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="c2cf6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c2cf6-109">EXAMPLES</span></span>

## <span data-ttu-id="c2cf6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2cf6-110">PARAMETERS</span></span>

### <span data-ttu-id="c2cf6-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="c2cf6-111">-CustomLogRawJson</span></span>
<span data-ttu-id="c2cf6-112">Az egyéni webhelycsoport-házirendet adja meg nyers JavaScript-objektumként (JSON) karakterláncként.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="c2cf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2cf6-113">-DefaultProfile</span></span>
<span data-ttu-id="c2cf6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c2cf6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2cf6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c2cf6-115">-Force</span></span>
<span data-ttu-id="c2cf6-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2cf6-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c2cf6-117">-Name</span></span>
<span data-ttu-id="c2cf6-118">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="c2cf6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2cf6-119">-ResourceGroupName</span></span>
<span data-ttu-id="c2cf6-120">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="c2cf6-121">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="c2cf6-121">-Workspace</span></span>
<span data-ttu-id="c2cf6-122">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c2cf6-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2cf6-123">-WorkspaceName</span></span>
<span data-ttu-id="c2cf6-124">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c2cf6-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c2cf6-125">-Confirm</span></span>
<span data-ttu-id="c2cf6-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2cf6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2cf6-127">-WhatIf</span></span>
<span data-ttu-id="c2cf6-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2cf6-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c2cf6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2cf6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cf6-130">CommonParameters</span></span>
<span data-ttu-id="c2cf6-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2cf6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cf6-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2cf6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cf6-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2cf6-133">INPUTS</span></span>

### <span data-ttu-id="c2cf6-134">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2cf6-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c2cf6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c2cf6-135">System.String</span></span>

## <span data-ttu-id="c2cf6-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2cf6-136">OUTPUTS</span></span>

### <span data-ttu-id="c2cf6-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c2cf6-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c2cf6-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2cf6-138">NOTES</span></span>

## <span data-ttu-id="c2cf6-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2cf6-139">RELATED LINKS</span></span>

[<span data-ttu-id="c2cf6-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="c2cf6-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="c2cf6-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="c2cf6-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


