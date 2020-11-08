---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 94706768c6e5f222abe5a74ea32549f356abe1c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185933"
---
# <span data-ttu-id="cfdba-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cfdba-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="cfdba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfdba-102">SYNOPSIS</span></span>
<span data-ttu-id="cfdba-103">Nem állítja be az egyéni naplók gyűjteményét a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="cfdba-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="cfdba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfdba-104">SYNTAX</span></span>

### <span data-ttu-id="cfdba-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cfdba-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfdba-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cfdba-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfdba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfdba-107">DESCRIPTION</span></span>
<span data-ttu-id="cfdba-108">A **disable-AzOperationalInsightsLinuxCustomLogCollection** parancsmag leállítja az egyéni naplók gyűjteményét a csatlakoztatott linuxos számítógépekről a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="cfdba-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="cfdba-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cfdba-109">EXAMPLES</span></span>

## <span data-ttu-id="cfdba-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfdba-110">PARAMETERS</span></span>

### <span data-ttu-id="cfdba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfdba-111">-DefaultProfile</span></span>
<span data-ttu-id="cfdba-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cfdba-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfdba-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfdba-113">-ResourceGroupName</span></span>
<span data-ttu-id="cfdba-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cfdba-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="cfdba-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="cfdba-115">-Workspace</span></span>
<span data-ttu-id="cfdba-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="cfdba-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cfdba-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cfdba-117">-WorkspaceName</span></span>
<span data-ttu-id="cfdba-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="cfdba-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cfdba-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cfdba-119">-Confirm</span></span>
<span data-ttu-id="cfdba-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfdba-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfdba-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfdba-121">-WhatIf</span></span>
<span data-ttu-id="cfdba-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cfdba-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfdba-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfdba-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfdba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfdba-124">CommonParameters</span></span>
<span data-ttu-id="cfdba-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfdba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfdba-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfdba-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfdba-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfdba-127">INPUTS</span></span>

### <span data-ttu-id="cfdba-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cfdba-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="cfdba-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cfdba-129">System.String</span></span>

## <span data-ttu-id="cfdba-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfdba-130">OUTPUTS</span></span>

### <span data-ttu-id="cfdba-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cfdba-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cfdba-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfdba-132">NOTES</span></span>
* <span data-ttu-id="cfdba-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="cfdba-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cfdba-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfdba-134">RELATED LINKS</span></span>

[<span data-ttu-id="cfdba-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cfdba-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


