---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5f3200459cbcca9806a1a7185798889b3457760d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498235"
---
# <span data-ttu-id="5affd-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="5affd-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="5affd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5affd-102">SYNOPSIS</span></span>
<span data-ttu-id="5affd-103">Begyűjti az eseménynaplókat a Windows operációs rendszert futtató számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="5affd-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5affd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5affd-104">SYNTAX</span></span>

### <span data-ttu-id="5affd-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5affd-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5affd-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5affd-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5affd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5affd-107">DESCRIPTION</span></span>
<span data-ttu-id="5affd-108">A **New-AzureRmOperationalInsightsWindowsEventDataSource** parancsmag olyan adatforrást ad hozzá, amely a Windows-eseménynaplókat gyűjti össze olyan csatlakoztatott számítógépekről, amelyek a Windows operációs rendszert futtatják az Azure hadműveleti vizsgálatokban.</span><span class="sxs-lookup"><span data-stu-id="5affd-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="5affd-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5affd-109">EXAMPLES</span></span>

## <span data-ttu-id="5affd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5affd-110">PARAMETERS</span></span>

### <span data-ttu-id="5affd-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="5affd-111">-CollectErrors</span></span>
<span data-ttu-id="5affd-112">Jelzi, hogy a műveleti elemzések hibaüzeneteket gyűjtenek.</span><span class="sxs-lookup"><span data-stu-id="5affd-112">Indicates that Operational Insights collects error messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5affd-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="5affd-113">-CollectInformation</span></span>
<span data-ttu-id="5affd-114">Jelzi, hogy az üzemi elemzések az információs üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="5affd-114">Indicates that Operational Insights collects information messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5affd-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="5affd-115">-CollectWarnings</span></span>
<span data-ttu-id="5affd-116">Jelzi, hogy a műveleti elemzések a figyelmeztető üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="5affd-116">Indicates that Operational Insights collects warning messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5affd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5affd-117">-DefaultProfile</span></span>
<span data-ttu-id="5affd-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5affd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5affd-119">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="5affd-119">-EventLogName</span></span>
<span data-ttu-id="5affd-120">Az Eseménynapló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5affd-120">Specifies the name of the event log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5affd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5affd-121">-Force</span></span>
<span data-ttu-id="5affd-122">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="5affd-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5affd-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5affd-123">-Name</span></span>
<span data-ttu-id="5affd-124">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5affd-124">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5affd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5affd-125">-ResourceGroupName</span></span>
<span data-ttu-id="5affd-126">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5affd-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="5affd-127">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="5affd-127">-Workspace</span></span>
<span data-ttu-id="5affd-128">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="5affd-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5affd-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5affd-129">-WorkspaceName</span></span>
<span data-ttu-id="5affd-130">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="5affd-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5affd-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5affd-131">-Confirm</span></span>
<span data-ttu-id="5affd-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5affd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5affd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5affd-133">-WhatIf</span></span>
<span data-ttu-id="5affd-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5affd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5affd-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5affd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5affd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5affd-136">CommonParameters</span></span>
<span data-ttu-id="5affd-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5affd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5affd-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5affd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5affd-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5affd-139">INPUTS</span></span>

### <span data-ttu-id="5affd-140">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5affd-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="5affd-141">Paraméterek: munkaterület (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5affd-141">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="5affd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5affd-142">System.String</span></span>

## <span data-ttu-id="5affd-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5affd-143">OUTPUTS</span></span>

### <span data-ttu-id="5affd-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5affd-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5affd-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5affd-145">NOTES</span></span>

## <span data-ttu-id="5affd-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5affd-146">RELATED LINKS</span></span>
