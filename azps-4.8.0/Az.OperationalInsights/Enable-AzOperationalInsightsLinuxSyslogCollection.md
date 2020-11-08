---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025131"
---
# <span data-ttu-id="50054-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="50054-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="50054-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50054-102">SYNOPSIS</span></span>
<span data-ttu-id="50054-103">Elindítja a syslog-adatgyűjteményt a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="50054-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="50054-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50054-104">SYNTAX</span></span>

### <span data-ttu-id="50054-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="50054-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50054-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="50054-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50054-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="50054-107">DESCRIPTION</span></span>
<span data-ttu-id="50054-108">Az **enable-AzOperationalInsightsLinuxSyslogCollection** parancsmag az összekapcsolt linuxos számítógépekről származó syslog-adatgyűjtést egy munkaterületről indítja el.</span><span class="sxs-lookup"><span data-stu-id="50054-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="50054-109">Példák</span><span class="sxs-lookup"><span data-stu-id="50054-109">EXAMPLES</span></span>

## <span data-ttu-id="50054-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50054-110">PARAMETERS</span></span>

### <span data-ttu-id="50054-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50054-111">-DefaultProfile</span></span>
<span data-ttu-id="50054-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="50054-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50054-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50054-113">-ResourceGroupName</span></span>
<span data-ttu-id="50054-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="50054-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="50054-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="50054-115">-Workspace</span></span>
<span data-ttu-id="50054-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="50054-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="50054-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="50054-117">-WorkspaceName</span></span>
<span data-ttu-id="50054-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="50054-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="50054-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="50054-119">-Confirm</span></span>
<span data-ttu-id="50054-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50054-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50054-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50054-121">-WhatIf</span></span>
<span data-ttu-id="50054-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="50054-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50054-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50054-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50054-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50054-124">CommonParameters</span></span>
<span data-ttu-id="50054-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50054-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50054-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50054-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50054-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50054-127">INPUTS</span></span>

### <span data-ttu-id="50054-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="50054-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="50054-129">System. String</span><span class="sxs-lookup"><span data-stu-id="50054-129">System.String</span></span>

## <span data-ttu-id="50054-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50054-130">OUTPUTS</span></span>

### <span data-ttu-id="50054-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="50054-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="50054-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50054-132">NOTES</span></span>
* <span data-ttu-id="50054-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="50054-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="50054-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50054-134">RELATED LINKS</span></span>

[<span data-ttu-id="50054-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="50054-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="50054-136">Új – AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="50054-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


