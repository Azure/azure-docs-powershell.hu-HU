---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/disable-azurermoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 2eecf19ad385729bfe0a140f234f2ddf5053e746
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494023"
---
# <span data-ttu-id="d4ab1-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d4ab1-101">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="d4ab1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ab1-103">Nem állítja be az egyéni naplók gyűjteményét a Linux rendszerű számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="d4ab1-103">Stops collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4ab1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4ab1-104">SYNTAX</span></span>

### <span data-ttu-id="d4ab1-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4ab1-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4ab1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d4ab1-106">ByWorkspaceObject</span></span>
```
Disable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4ab1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4ab1-107">DESCRIPTION</span></span>
<span data-ttu-id="d4ab1-108">A **disable-AzureRmOperationalInsightsLinuxCustomLogCollection** parancsmag leállítja az egyéni naplók gyűjteményét a csatlakoztatott linuxos számítógépekről a munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="d4ab1-108">The **Disable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="d4ab1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d4ab1-109">EXAMPLES</span></span>

## <span data-ttu-id="d4ab1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4ab1-110">PARAMETERS</span></span>

### <span data-ttu-id="d4ab1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ab1-111">-DefaultProfile</span></span>
<span data-ttu-id="d4ab1-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d4ab1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4ab1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ab1-113">-ResourceGroupName</span></span>
<span data-ttu-id="d4ab1-114">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4ab1-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="d4ab1-115">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="d4ab1-115">-Workspace</span></span>
<span data-ttu-id="d4ab1-116">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d4ab1-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d4ab1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d4ab1-117">-WorkspaceName</span></span>
<span data-ttu-id="d4ab1-118">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="d4ab1-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d4ab1-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d4ab1-119">-Confirm</span></span>
<span data-ttu-id="d4ab1-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d4ab1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4ab1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4ab1-121">-WhatIf</span></span>
<span data-ttu-id="d4ab1-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d4ab1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4ab1-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d4ab1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4ab1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ab1-124">CommonParameters</span></span>
<span data-ttu-id="d4ab1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4ab1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ab1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4ab1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ab1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4ab1-127">INPUTS</span></span>

### <span data-ttu-id="d4ab1-128">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d4ab1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="d4ab1-129">Paraméterek: munkaterület (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4ab1-129">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="d4ab1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d4ab1-130">System.String</span></span>

## <span data-ttu-id="d4ab1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4ab1-131">OUTPUTS</span></span>

### <span data-ttu-id="d4ab1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d4ab1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d4ab1-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4ab1-133">NOTES</span></span>
* <span data-ttu-id="d4ab1-134">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="d4ab1-134">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d4ab1-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4ab1-135">RELATED LINKS</span></span>

[<span data-ttu-id="d4ab1-136">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="d4ab1-136">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


