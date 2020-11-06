---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 1e9114b9f6b62f6900c975b39e5f8c67b4d9051a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494763"
---
# <span data-ttu-id="ce477-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="ce477-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="ce477-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ce477-102">SYNOPSIS</span></span>
<span data-ttu-id="ce477-103">Teljesítményszámlálókat ad hozzá a munkaterületek minden linuxos számítógépéhez.</span><span class="sxs-lookup"><span data-stu-id="ce477-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce477-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ce477-104">SYNTAX</span></span>

### <span data-ttu-id="ce477-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ce477-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce477-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ce477-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce477-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ce477-107">DESCRIPTION</span></span>
<span data-ttu-id="ce477-108">A **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** parancsmag olyan teljesítményszámlálókat ad eredményül, amelyekben az Azure-műveletek a munkaterületek összes linuxos számítógépére gyűjtik az adatokat.</span><span class="sxs-lookup"><span data-stu-id="ce477-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="ce477-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ce477-109">EXAMPLES</span></span>

## <span data-ttu-id="ce477-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ce477-110">PARAMETERS</span></span>

### <span data-ttu-id="ce477-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="ce477-111">-CounterNames</span></span>
<span data-ttu-id="ce477-112">A számlálók neveinek tömbjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce477-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce477-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ce477-113">-Force</span></span>
<span data-ttu-id="ce477-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ce477-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce477-115">-Példánynév</span><span class="sxs-lookup"><span data-stu-id="ce477-115">-InstanceName</span></span>
<span data-ttu-id="ce477-116">A példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce477-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="ce477-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="ce477-117">-IntervalSeconds</span></span>
<span data-ttu-id="ce477-118">A gyűjtemény intervallumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce477-118">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="ce477-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ce477-119">-Name</span></span>
<span data-ttu-id="ce477-120">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce477-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="ce477-121">-Objektumnév</span><span class="sxs-lookup"><span data-stu-id="ce477-121">-ObjectName</span></span>
<span data-ttu-id="ce477-122">Az objektum nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce477-122">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="ce477-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce477-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce477-124">A Linux-számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ce477-124">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="ce477-125">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="ce477-125">-Workspace</span></span>
<span data-ttu-id="ce477-126">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="ce477-126">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ce477-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce477-127">-WorkspaceName</span></span>
<span data-ttu-id="ce477-128">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="ce477-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ce477-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ce477-129">-Confirm</span></span>
<span data-ttu-id="ce477-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ce477-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce477-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce477-131">-WhatIf</span></span>
<span data-ttu-id="ce477-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ce477-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce477-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ce477-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce477-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce477-134">-DefaultProfile</span></span>
<span data-ttu-id="ce477-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ce477-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce477-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce477-136">CommonParameters</span></span>
<span data-ttu-id="ce477-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ce477-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce477-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce477-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce477-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce477-139">INPUTS</span></span>

### <span data-ttu-id="ce477-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce477-140">PSWorkspace</span></span>
<span data-ttu-id="ce477-141">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ce477-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="ce477-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ce477-142">OUTPUTS</span></span>

### <span data-ttu-id="ce477-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ce477-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ce477-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ce477-144">NOTES</span></span>

## <span data-ttu-id="ce477-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ce477-145">RELATED LINKS</span></span>

[<span data-ttu-id="ce477-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="ce477-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="ce477-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="ce477-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


