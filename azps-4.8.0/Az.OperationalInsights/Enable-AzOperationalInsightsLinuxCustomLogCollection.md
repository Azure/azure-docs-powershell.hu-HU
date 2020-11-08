---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0cd64af058ecf9bbc1f42178d263fcf20cabc75f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184310"
---
# <span data-ttu-id="fb989-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fb989-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="fb989-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb989-102">SYNOPSIS</span></span>
<span data-ttu-id="fb989-103">Elindítja az egyéni naplók gyűjteményét a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="fb989-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="fb989-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb989-104">SYNTAX</span></span>

### <span data-ttu-id="fb989-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fb989-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb989-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fb989-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb989-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb989-107">DESCRIPTION</span></span>
<span data-ttu-id="fb989-108">Az **enable-AzOperationalInsightsLinuxCustomLogCollection** parancsmag az egyéni naplók gyűjteményét az összekapcsolt linuxos számítógépekről indítja el egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="fb989-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="fb989-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fb989-109">EXAMPLES</span></span>

## <span data-ttu-id="fb989-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb989-110">PARAMETERS</span></span>

### <span data-ttu-id="fb989-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb989-111">-DefaultProfile</span></span>
<span data-ttu-id="fb989-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fb989-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb989-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb989-113">-ResourceGroupName</span></span>
<span data-ttu-id="fb989-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb989-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="fb989-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="fb989-115">-Workspace</span></span>
<span data-ttu-id="fb989-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="fb989-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fb989-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb989-117">-WorkspaceName</span></span>
<span data-ttu-id="fb989-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="fb989-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fb989-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb989-119">-Confirm</span></span>
<span data-ttu-id="fb989-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb989-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb989-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb989-121">-WhatIf</span></span>
<span data-ttu-id="fb989-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb989-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb989-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb989-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb989-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb989-124">CommonParameters</span></span>
<span data-ttu-id="fb989-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb989-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb989-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb989-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb989-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb989-127">INPUTS</span></span>

### <span data-ttu-id="fb989-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fb989-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="fb989-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fb989-129">System.String</span></span>

## <span data-ttu-id="fb989-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb989-130">OUTPUTS</span></span>

### <span data-ttu-id="fb989-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fb989-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fb989-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb989-132">NOTES</span></span>
* <span data-ttu-id="fb989-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="fb989-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fb989-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb989-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb989-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="fb989-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


