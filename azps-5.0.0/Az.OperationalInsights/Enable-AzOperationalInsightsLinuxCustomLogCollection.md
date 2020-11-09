---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0cd64af058ecf9bbc1f42178d263fcf20cabc75f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303467"
---
# <span data-ttu-id="42534-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="42534-101">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="42534-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="42534-102">SYNOPSIS</span></span>
<span data-ttu-id="42534-103">Elindítja az egyéni naplók gyűjteményét a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="42534-103">Starts collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="42534-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="42534-104">SYNTAX</span></span>

### <span data-ttu-id="42534-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="42534-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42534-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="42534-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42534-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="42534-107">DESCRIPTION</span></span>
<span data-ttu-id="42534-108">Az **enable-AzOperationalInsightsLinuxCustomLogCollection** parancsmag az egyéni naplók gyűjteményét az összekapcsolt linuxos számítógépekről indítja el egy munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="42534-108">The **Enable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="42534-109">Példák</span><span class="sxs-lookup"><span data-stu-id="42534-109">EXAMPLES</span></span>

## <span data-ttu-id="42534-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="42534-110">PARAMETERS</span></span>

### <span data-ttu-id="42534-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42534-111">-DefaultProfile</span></span>
<span data-ttu-id="42534-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="42534-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42534-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42534-113">-ResourceGroupName</span></span>
<span data-ttu-id="42534-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="42534-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="42534-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="42534-115">-Workspace</span></span>
<span data-ttu-id="42534-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="42534-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="42534-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="42534-117">-WorkspaceName</span></span>
<span data-ttu-id="42534-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="42534-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="42534-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="42534-119">-Confirm</span></span>
<span data-ttu-id="42534-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="42534-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42534-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42534-121">-WhatIf</span></span>
<span data-ttu-id="42534-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="42534-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42534-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="42534-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42534-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42534-124">CommonParameters</span></span>
<span data-ttu-id="42534-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="42534-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42534-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42534-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42534-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="42534-127">INPUTS</span></span>

### <span data-ttu-id="42534-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="42534-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="42534-129">System. String</span><span class="sxs-lookup"><span data-stu-id="42534-129">System.String</span></span>

## <span data-ttu-id="42534-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="42534-130">OUTPUTS</span></span>

### <span data-ttu-id="42534-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="42534-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="42534-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="42534-132">NOTES</span></span>
* <span data-ttu-id="42534-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="42534-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="42534-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="42534-134">RELATED LINKS</span></span>

[<span data-ttu-id="42534-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="42534-135">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)


