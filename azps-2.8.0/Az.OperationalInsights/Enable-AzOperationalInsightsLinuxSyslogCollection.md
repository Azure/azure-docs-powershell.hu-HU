---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 351a24f2307a09422df4c923b3088f6a39661fd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838475"
---
# <span data-ttu-id="0e1df-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="0e1df-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="0e1df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e1df-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1df-103">Elindítja a syslog-adatgyűjteményt a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="0e1df-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="0e1df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e1df-104">SYNTAX</span></span>

### <span data-ttu-id="0e1df-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e1df-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e1df-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0e1df-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e1df-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e1df-107">DESCRIPTION</span></span>
<span data-ttu-id="0e1df-108">Az **enable-AzOperationalInsightsLinuxSyslogCollection** parancsmag az összekapcsolt linuxos számítógépekről származó syslog-adatgyűjtést egy munkaterületről indítja el.</span><span class="sxs-lookup"><span data-stu-id="0e1df-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="0e1df-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0e1df-109">EXAMPLES</span></span>

## <span data-ttu-id="0e1df-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e1df-110">PARAMETERS</span></span>

### <span data-ttu-id="0e1df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1df-111">-DefaultProfile</span></span>
<span data-ttu-id="0e1df-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0e1df-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e1df-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e1df-113">-ResourceGroupName</span></span>
<span data-ttu-id="0e1df-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e1df-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="0e1df-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="0e1df-115">-Workspace</span></span>
<span data-ttu-id="0e1df-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="0e1df-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0e1df-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0e1df-117">-WorkspaceName</span></span>
<span data-ttu-id="0e1df-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="0e1df-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="0e1df-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0e1df-119">-Confirm</span></span>
<span data-ttu-id="0e1df-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0e1df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e1df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e1df-121">-WhatIf</span></span>
<span data-ttu-id="0e1df-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0e1df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e1df-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e1df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e1df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1df-124">CommonParameters</span></span>
<span data-ttu-id="0e1df-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e1df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1df-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1df-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1df-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e1df-127">INPUTS</span></span>

### <span data-ttu-id="0e1df-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e1df-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="0e1df-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0e1df-129">System.String</span></span>

## <span data-ttu-id="0e1df-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e1df-130">OUTPUTS</span></span>

### <span data-ttu-id="0e1df-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0e1df-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0e1df-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e1df-132">NOTES</span></span>
* <span data-ttu-id="0e1df-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="0e1df-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0e1df-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e1df-134">RELATED LINKS</span></span>

[<span data-ttu-id="0e1df-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="0e1df-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="0e1df-136">Új – AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="0e1df-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


