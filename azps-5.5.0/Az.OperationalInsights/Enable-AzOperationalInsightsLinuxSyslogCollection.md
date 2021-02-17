---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156659"
---
# <span data-ttu-id="23b2a-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="23b2a-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="23b2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="23b2a-103">Elindítja a syslog adatok gyűjtését Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="23b2a-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="23b2a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="23b2a-104">SYNTAX</span></span>

### <span data-ttu-id="23b2a-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="23b2a-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23b2a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="23b2a-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23b2a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="23b2a-107">DESCRIPTION</span></span>
<span data-ttu-id="23b2a-108">Az **Enable-AzOperationalInsightsLinuxSyslogCollection parancsmag** elindítja a syslog adatok gyűjteményét a csatlakoztatott Linux számítógépekről egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="23b2a-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="23b2a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="23b2a-109">EXAMPLES</span></span>

## <span data-ttu-id="23b2a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23b2a-110">PARAMETERS</span></span>

### <span data-ttu-id="23b2a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b2a-111">-DefaultProfile</span></span>
<span data-ttu-id="23b2a-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="23b2a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23b2a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b2a-113">-ResourceGroupName</span></span>
<span data-ttu-id="23b2a-114">Egy Linux rendszerű számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="23b2a-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="23b2a-115">-Workspace</span><span class="sxs-lookup"><span data-stu-id="23b2a-115">-Workspace</span></span>
<span data-ttu-id="23b2a-116">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="23b2a-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="23b2a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23b2a-117">-WorkspaceName</span></span>
<span data-ttu-id="23b2a-118">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="23b2a-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="23b2a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23b2a-119">-Confirm</span></span>
<span data-ttu-id="23b2a-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="23b2a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23b2a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23b2a-121">-WhatIf</span></span>
<span data-ttu-id="23b2a-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="23b2a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23b2a-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23b2a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23b2a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b2a-124">CommonParameters</span></span>
<span data-ttu-id="23b2a-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b2a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b2a-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23b2a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b2a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23b2a-127">INPUTS</span></span>

### <span data-ttu-id="23b2a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="23b2a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="23b2a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="23b2a-129">System.String</span></span>

## <span data-ttu-id="23b2a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23b2a-130">OUTPUTS</span></span>

### <span data-ttu-id="23b2a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="23b2a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="23b2a-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="23b2a-132">NOTES</span></span>
* <span data-ttu-id="23b2a-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="23b2a-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="23b2a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23b2a-134">RELATED LINKS</span></span>

[<span data-ttu-id="23b2a-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="23b2a-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="23b2a-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="23b2a-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


