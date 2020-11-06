---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 49d465b1d993542790c20833ff5b1f75e03d5f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505412"
---
# <span data-ttu-id="31150-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="31150-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="31150-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31150-102">SYNOPSIS</span></span>
<span data-ttu-id="31150-103">Adatforrást ad hozzá a linuxos számítógépekhez.</span><span class="sxs-lookup"><span data-stu-id="31150-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31150-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31150-104">SYNTAX</span></span>

### <span data-ttu-id="31150-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31150-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31150-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="31150-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31150-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="31150-107">DESCRIPTION</span></span>
<span data-ttu-id="31150-108">A **New-AzureRmOperationalInsightsLinuxSyslogDataSource** parancsmag a syslog-adatforrást felveszi egy munkaterületen összekapcsolt linuxos számítógépekre.</span><span class="sxs-lookup"><span data-stu-id="31150-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="31150-109">Az Azure hadműveleti ismeretei a syslog-adatok gyűjtésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="31150-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="31150-110">Példák</span><span class="sxs-lookup"><span data-stu-id="31150-110">EXAMPLES</span></span>

## <span data-ttu-id="31150-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31150-111">PARAMETERS</span></span>

### <span data-ttu-id="31150-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="31150-112">-CollectAlert</span></span>
<span data-ttu-id="31150-113">Jelzi, hogy a műveleti elemzések begyűjtik a riasztási üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="31150-113">Indicates that Operational Insights collects alert messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="31150-114">-CollectCritical</span></span>
<span data-ttu-id="31150-115">Jelzi, hogy a műveletek a kritikus üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="31150-115">Indicates that Operational Insights collects critical messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="31150-116">-CollectDebug</span></span>
<span data-ttu-id="31150-117">Jelzi, hogy a műveletek a hibakeresési üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="31150-117">Indicates that Operational Insights collects debug messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="31150-118">-CollectEmergency</span></span>
<span data-ttu-id="31150-119">Jelzi, hogy a tevékenységi összefüggések a vészhelyzeti üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="31150-119">Indicates that Operational Insights collects emergency messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="31150-120">-CollectError</span></span>
<span data-ttu-id="31150-121">Jelzi, hogy a műveleti elemzések hibaüzeneteket gyűjtenek.</span><span class="sxs-lookup"><span data-stu-id="31150-121">Indicates that Operational Insights collects error messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="31150-122">-CollectInformational</span></span>
<span data-ttu-id="31150-123">Jelzi, hogy a műveleti elemzések gyűjtik az információs üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="31150-123">Indicates that Operational Insights collects informational messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="31150-124">-CollectNotice</span></span>
<span data-ttu-id="31150-125">Jelzi, hogy az üzemeltetési elemzések összegyűjtik az üzeneteket.</span><span class="sxs-lookup"><span data-stu-id="31150-125">Indicates that Operational Insights collects notice messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="31150-126">-CollectWarning</span></span>
<span data-ttu-id="31150-127">Jelzi, hogy a syslog figyelmeztető üzeneteket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="31150-127">Indicates that the syslog includes warning messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31150-128">-DefaultProfile</span></span>
<span data-ttu-id="31150-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="31150-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-130">-Létesítmény</span><span class="sxs-lookup"><span data-stu-id="31150-130">-Facility</span></span>
<span data-ttu-id="31150-131">Egy eszköz kódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="31150-131">Specifies a facility code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31150-132">-Force</span><span class="sxs-lookup"><span data-stu-id="31150-132">-Force</span></span>
<span data-ttu-id="31150-133">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="31150-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="31150-134">-Name</span></span>
<span data-ttu-id="31150-135">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31150-135">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31150-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31150-136">-ResourceGroupName</span></span>
<span data-ttu-id="31150-137">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31150-137">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31150-138">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="31150-138">-Workspace</span></span>
<span data-ttu-id="31150-139">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="31150-139">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31150-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31150-140">-WorkspaceName</span></span>
<span data-ttu-id="31150-141">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="31150-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31150-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="31150-142">-Confirm</span></span>
<span data-ttu-id="31150-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31150-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31150-144">-WhatIf</span></span>
<span data-ttu-id="31150-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="31150-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31150-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31150-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31150-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31150-147">CommonParameters</span></span>
<span data-ttu-id="31150-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31150-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31150-149">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31150-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31150-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31150-150">INPUTS</span></span>

### <span data-ttu-id="31150-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="31150-151">PSWorkspace</span></span>
<span data-ttu-id="31150-152">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="31150-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="31150-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31150-153">OUTPUTS</span></span>

### <span data-ttu-id="31150-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="31150-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="31150-155">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31150-155">NOTES</span></span>

## <span data-ttu-id="31150-156">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31150-156">RELATED LINKS</span></span>

[<span data-ttu-id="31150-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="31150-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="31150-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="31150-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


