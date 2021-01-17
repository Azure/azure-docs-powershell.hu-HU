---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481093"
---
# <span data-ttu-id="36f28-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="36f28-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="36f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f28-102">SYNOPSIS</span></span>
<span data-ttu-id="36f28-103">Elindítja a syslog adatok gyűjtését Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="36f28-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="36f28-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="36f28-104">SYNTAX</span></span>

### <span data-ttu-id="36f28-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36f28-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f28-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="36f28-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36f28-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="36f28-107">DESCRIPTION</span></span>
<span data-ttu-id="36f28-108">Az **Enable-AzOperationalInsightsLinuxSyslogCollection parancsmag** elindítja a syslog adatok gyűjteményét a csatlakoztatott Linux számítógépekről egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="36f28-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="36f28-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="36f28-109">EXAMPLES</span></span>

## <span data-ttu-id="36f28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36f28-110">PARAMETERS</span></span>

### <span data-ttu-id="36f28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f28-111">-DefaultProfile</span></span>
<span data-ttu-id="36f28-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="36f28-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36f28-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f28-113">-ResourceGroupName</span></span>
<span data-ttu-id="36f28-114">Egy Linux rendszerű számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="36f28-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="36f28-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="36f28-115">-Workspace</span></span>
<span data-ttu-id="36f28-116">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="36f28-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="36f28-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="36f28-117">-WorkspaceName</span></span>
<span data-ttu-id="36f28-118">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="36f28-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="36f28-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36f28-119">-Confirm</span></span>
<span data-ttu-id="36f28-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="36f28-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f28-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f28-121">-WhatIf</span></span>
<span data-ttu-id="36f28-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="36f28-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36f28-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36f28-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f28-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f28-124">CommonParameters</span></span>
<span data-ttu-id="36f28-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f28-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f28-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f28-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f28-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36f28-127">INPUTS</span></span>

### <span data-ttu-id="36f28-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="36f28-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="36f28-129">System.String</span><span class="sxs-lookup"><span data-stu-id="36f28-129">System.String</span></span>

## <span data-ttu-id="36f28-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36f28-130">OUTPUTS</span></span>

### <span data-ttu-id="36f28-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="36f28-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="36f28-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="36f28-132">NOTES</span></span>
* <span data-ttu-id="36f28-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="36f28-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="36f28-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36f28-134">RELATED LINKS</span></span>

[<span data-ttu-id="36f28-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="36f28-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="36f28-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="36f28-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


