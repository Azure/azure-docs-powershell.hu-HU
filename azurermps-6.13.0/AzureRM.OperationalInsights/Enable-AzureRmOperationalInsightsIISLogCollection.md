---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: b76e17169bdea8e25c1b861cd7de802d877455f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494020"
---
# <span data-ttu-id="12335-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="12335-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="12335-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12335-102">SYNOPSIS</span></span>
<span data-ttu-id="12335-103">Elindítja az IIS-naplók gyűjteményét a munkaterületen lévő számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="12335-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12335-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12335-104">SYNTAX</span></span>

### <span data-ttu-id="12335-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="12335-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12335-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="12335-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12335-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="12335-107">DESCRIPTION</span></span>
<span data-ttu-id="12335-108">Az **enable-AzureRmOperationalInsightsIISLogCollection** parancsmag az Internet Information Services (IIS) naplóit a munkaterületen lévő csatlakoztatott számítógépekről indítja el.</span><span class="sxs-lookup"><span data-stu-id="12335-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="12335-109">Példák</span><span class="sxs-lookup"><span data-stu-id="12335-109">EXAMPLES</span></span>

## <span data-ttu-id="12335-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12335-110">PARAMETERS</span></span>

### <span data-ttu-id="12335-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12335-111">-DefaultProfile</span></span>
<span data-ttu-id="12335-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="12335-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12335-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12335-113">-ResourceGroupName</span></span>
<span data-ttu-id="12335-114">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="12335-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="12335-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="12335-115">-Workspace</span></span>
<span data-ttu-id="12335-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="12335-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="12335-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="12335-117">-WorkspaceName</span></span>
<span data-ttu-id="12335-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="12335-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="12335-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12335-119">-Confirm</span></span>
<span data-ttu-id="12335-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12335-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12335-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12335-121">-WhatIf</span></span>
<span data-ttu-id="12335-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12335-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12335-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12335-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12335-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12335-124">CommonParameters</span></span>
<span data-ttu-id="12335-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12335-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12335-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12335-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12335-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12335-127">INPUTS</span></span>

### <span data-ttu-id="12335-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="12335-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="12335-129">Paraméterek: munkaterület (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12335-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="12335-130">System. String</span><span class="sxs-lookup"><span data-stu-id="12335-130">System.String</span></span>

## <span data-ttu-id="12335-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12335-131">OUTPUTS</span></span>

### <span data-ttu-id="12335-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="12335-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="12335-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12335-133">NOTES</span></span>

## <span data-ttu-id="12335-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12335-134">RELATED LINKS</span></span>

[<span data-ttu-id="12335-135">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="12335-135">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


