---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: f5bc73ee6fc2f3c20b92f8780bcddec99bc46fee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93844974"
---
# <span data-ttu-id="6a9a3-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="6a9a3-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="6a9a3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6a9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9a3-103">Nem állítja be a syslog-adatgyűjtést a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="6a9a3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6a9a3-104">SYNTAX</span></span>

### <span data-ttu-id="6a9a3-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a9a3-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a9a3-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a9a3-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a9a3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="6a9a3-107">DESCRIPTION</span></span>
<span data-ttu-id="6a9a3-108">A **disable-AzOperationalInsightsLinuxSyslogCollection** parancsmag nem gyűjti össze a syslog-adatforrásokat a csatlakoztatott linuxos számítógépekről egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="6a9a3-109">Példák</span><span class="sxs-lookup"><span data-stu-id="6a9a3-109">EXAMPLES</span></span>

## <span data-ttu-id="6a9a3-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6a9a3-110">PARAMETERS</span></span>

### <span data-ttu-id="6a9a3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9a3-111">-DefaultProfile</span></span>
<span data-ttu-id="6a9a3-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6a9a3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a9a3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9a3-113">-ResourceGroupName</span></span>
<span data-ttu-id="6a9a3-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="6a9a3-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="6a9a3-115">-Workspace</span></span>
<span data-ttu-id="6a9a3-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6a9a3-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a9a3-117">-WorkspaceName</span></span>
<span data-ttu-id="6a9a3-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6a9a3-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6a9a3-119">-Confirm</span></span>
<span data-ttu-id="6a9a3-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a9a3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a9a3-121">-WhatIf</span></span>
<span data-ttu-id="6a9a3-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a9a3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6a9a3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a9a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9a3-124">CommonParameters</span></span>
<span data-ttu-id="6a9a3-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6a9a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9a3-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9a3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9a3-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a9a3-127">INPUTS</span></span>

### <span data-ttu-id="6a9a3-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a9a3-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6a9a3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6a9a3-129">System.String</span></span>

## <span data-ttu-id="6a9a3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a9a3-130">OUTPUTS</span></span>

### <span data-ttu-id="6a9a3-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6a9a3-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6a9a3-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6a9a3-132">NOTES</span></span>
* <span data-ttu-id="6a9a3-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="6a9a3-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="6a9a3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a9a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="6a9a3-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="6a9a3-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="6a9a3-136">Új – AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="6a9a3-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


