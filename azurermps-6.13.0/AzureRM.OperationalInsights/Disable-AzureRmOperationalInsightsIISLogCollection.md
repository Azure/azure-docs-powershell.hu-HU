---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 085aa91321f9e263e4fa5620f982beb01eab2b16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672240"
---
# <span data-ttu-id="fd00d-101">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="fd00d-101">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="fd00d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fd00d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd00d-103">Nem állítja be az IIS-naplók gyűjteményét a számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="fd00d-103">Stops collection of IIS logs from computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd00d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fd00d-104">SYNTAX</span></span>

### <span data-ttu-id="fd00d-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fd00d-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd00d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fd00d-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd00d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fd00d-107">DESCRIPTION</span></span>
<span data-ttu-id="fd00d-108">A **disable-AzureRmOperationalInsightsIISLogCollection** parancsmag leállítja az Internet Information Services (IIS) naplózását egy munkaterületről csatlakoztatott számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="fd00d-108">The **Disable-AzureRmOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="fd00d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fd00d-109">EXAMPLES</span></span>

## <span data-ttu-id="fd00d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fd00d-110">PARAMETERS</span></span>

### <span data-ttu-id="fd00d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd00d-111">-DefaultProfile</span></span>
<span data-ttu-id="fd00d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fd00d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd00d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd00d-113">-ResourceGroupName</span></span>
<span data-ttu-id="fd00d-114">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fd00d-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="fd00d-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="fd00d-115">-Workspace</span></span>
<span data-ttu-id="fd00d-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="fd00d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fd00d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd00d-117">-WorkspaceName</span></span>
<span data-ttu-id="fd00d-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="fd00d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fd00d-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fd00d-119">-Confirm</span></span>
<span data-ttu-id="fd00d-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fd00d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd00d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd00d-121">-WhatIf</span></span>
<span data-ttu-id="fd00d-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fd00d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd00d-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fd00d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd00d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd00d-124">CommonParameters</span></span>
<span data-ttu-id="fd00d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fd00d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd00d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd00d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd00d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd00d-127">INPUTS</span></span>

### <span data-ttu-id="fd00d-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd00d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="fd00d-129">Paraméterek: munkaterület (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd00d-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="fd00d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fd00d-130">System.String</span></span>

## <span data-ttu-id="fd00d-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fd00d-131">OUTPUTS</span></span>

### <span data-ttu-id="fd00d-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fd00d-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fd00d-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fd00d-133">NOTES</span></span>
* <span data-ttu-id="fd00d-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="fd00d-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fd00d-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fd00d-135">RELATED LINKS</span></span>

[<span data-ttu-id="fd00d-136">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="fd00d-136">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Enable-AzureRmOperationalInsightsIISLogCollection.md)


