---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 71a0089b4f593032404b71f17ba432486f5498d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188084"
---
# <span data-ttu-id="ef1e1-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="ef1e1-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="ef1e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ef1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1e1-103">Nem állítja be az IIS-naplók gyűjteményét a számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="ef1e1-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="ef1e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ef1e1-104">SYNTAX</span></span>

### <span data-ttu-id="ef1e1-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ef1e1-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef1e1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ef1e1-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef1e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ef1e1-107">DESCRIPTION</span></span>
<span data-ttu-id="ef1e1-108">A **disable-AzOperationalInsightsIISLogCollection** parancsmag leállítja az Internet Information Services (IIS) naplózását egy munkaterületről csatlakoztatott számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="ef1e1-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="ef1e1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ef1e1-109">EXAMPLES</span></span>

## <span data-ttu-id="ef1e1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ef1e1-110">PARAMETERS</span></span>

### <span data-ttu-id="ef1e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1e1-111">-DefaultProfile</span></span>
<span data-ttu-id="ef1e1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ef1e1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef1e1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1e1-113">-ResourceGroupName</span></span>
<span data-ttu-id="ef1e1-114">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ef1e1-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="ef1e1-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="ef1e1-115">-Workspace</span></span>
<span data-ttu-id="ef1e1-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="ef1e1-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ef1e1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ef1e1-117">-WorkspaceName</span></span>
<span data-ttu-id="ef1e1-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="ef1e1-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ef1e1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ef1e1-119">-Confirm</span></span>
<span data-ttu-id="ef1e1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ef1e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef1e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef1e1-121">-WhatIf</span></span>
<span data-ttu-id="ef1e1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ef1e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef1e1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ef1e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef1e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1e1-124">CommonParameters</span></span>
<span data-ttu-id="ef1e1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ef1e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1e1-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1e1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1e1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef1e1-127">INPUTS</span></span>

### <span data-ttu-id="ef1e1-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ef1e1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ef1e1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ef1e1-129">System.String</span></span>

## <span data-ttu-id="ef1e1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ef1e1-130">OUTPUTS</span></span>

### <span data-ttu-id="ef1e1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ef1e1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ef1e1-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ef1e1-132">NOTES</span></span>
* <span data-ttu-id="ef1e1-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="ef1e1-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ef1e1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ef1e1-134">RELATED LINKS</span></span>

[<span data-ttu-id="ef1e1-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="ef1e1-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)

