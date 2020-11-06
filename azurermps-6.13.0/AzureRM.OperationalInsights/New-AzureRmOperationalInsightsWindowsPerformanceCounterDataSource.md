---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 5a772007850342bd400666a5815d6d8b936f7c5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498228"
---
# <span data-ttu-id="28729-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="28729-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="28729-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="28729-102">SYNOPSIS</span></span>
<span data-ttu-id="28729-103">Windows teljesítményszámláló-adatforrást ad hozzá a Windows operációs rendszert futtató csatlakoztatott számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="28729-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28729-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="28729-104">SYNTAX</span></span>

### <span data-ttu-id="28729-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="28729-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28729-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="28729-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28729-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="28729-107">DESCRIPTION</span></span>
<span data-ttu-id="28729-108">A **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** parancsmag hozzáadja a Windows teljesítményszámláló-adatforrást a Windows operációs rendszert futtató csatlakoztatott számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="28729-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="28729-109">Példák</span><span class="sxs-lookup"><span data-stu-id="28729-109">EXAMPLES</span></span>

## <span data-ttu-id="28729-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="28729-110">PARAMETERS</span></span>

### <span data-ttu-id="28729-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="28729-111">-CounterName</span></span>
<span data-ttu-id="28729-112">A számláló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28729-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28729-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28729-113">-DefaultProfile</span></span>
<span data-ttu-id="28729-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="28729-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28729-115">-Force</span><span class="sxs-lookup"><span data-stu-id="28729-115">-Force</span></span>
<span data-ttu-id="28729-116">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="28729-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28729-117">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="28729-117">-InstanceName</span></span>
<span data-ttu-id="28729-118">A példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28729-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28729-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="28729-119">-IntervalSeconds</span></span>
<span data-ttu-id="28729-120">A gyűjtemény intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="28729-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28729-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="28729-121">-Name</span></span>
<span data-ttu-id="28729-122">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28729-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="28729-123">-Objektumnév</span><span class="sxs-lookup"><span data-stu-id="28729-123">-ObjectName</span></span>
<span data-ttu-id="28729-124">Az objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28729-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="28729-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28729-125">-ResourceGroupName</span></span>
<span data-ttu-id="28729-126">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="28729-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="28729-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="28729-127">-UseLegacyCollector</span></span>
<span data-ttu-id="28729-128">Használja az örökölt gyűjtőt vagy az alapértelmezett kollektorot.</span><span class="sxs-lookup"><span data-stu-id="28729-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="28729-129">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="28729-129">-Workspace</span></span>
<span data-ttu-id="28729-130">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="28729-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="28729-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28729-131">-WorkspaceName</span></span>
<span data-ttu-id="28729-132">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="28729-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="28729-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="28729-133">-Confirm</span></span>
<span data-ttu-id="28729-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="28729-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28729-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28729-135">-WhatIf</span></span>
<span data-ttu-id="28729-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="28729-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28729-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="28729-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28729-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28729-138">CommonParameters</span></span>
<span data-ttu-id="28729-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="28729-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28729-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28729-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28729-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="28729-141">INPUTS</span></span>

### <span data-ttu-id="28729-142">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="28729-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="28729-143">Paraméterek: munkaterület (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28729-143">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="28729-144">System. String</span><span class="sxs-lookup"><span data-stu-id="28729-144">System.String</span></span>

### <span data-ttu-id="28729-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="28729-145">System.Int32</span></span>

## <span data-ttu-id="28729-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="28729-146">OUTPUTS</span></span>

### <span data-ttu-id="28729-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="28729-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="28729-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="28729-148">NOTES</span></span>

## <span data-ttu-id="28729-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="28729-149">RELATED LINKS</span></span>
