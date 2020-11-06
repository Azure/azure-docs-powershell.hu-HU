---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: c82388dbfebb33c840b1c1066e41ab6c022e87d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494759"
---
# <span data-ttu-id="88780-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="88780-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="88780-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="88780-102">SYNOPSIS</span></span>
<span data-ttu-id="88780-103">Begyűjti az eseménynaplókat a Windows operációs rendszert futtató számítógépekről.</span><span class="sxs-lookup"><span data-stu-id="88780-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88780-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="88780-104">SYNTAX</span></span>

### <span data-ttu-id="88780-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="88780-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88780-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="88780-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88780-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="88780-107">DESCRIPTION</span></span>
<span data-ttu-id="88780-108">A **New-AzureRmOperationalInsightsWindowsEventDataSource** parancsmag olyan adatforrást ad hozzá, amely a Windows-eseménynaplókat gyűjti össze olyan csatlakoztatott számítógépekről, amelyek a Windows operációs rendszert futtatják az Azure hadműveleti vizsgálatokban.</span><span class="sxs-lookup"><span data-stu-id="88780-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="88780-109">Példák</span><span class="sxs-lookup"><span data-stu-id="88780-109">EXAMPLES</span></span>

## <span data-ttu-id="88780-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="88780-110">PARAMETERS</span></span>

### <span data-ttu-id="88780-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="88780-111">-CollectErrors</span></span>
<span data-ttu-id="88780-112">Jelzi, hogy a műveleti elemzések hibaüzeneteket gyűjtenek.</span><span class="sxs-lookup"><span data-stu-id="88780-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="88780-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="88780-113">-CollectInformation</span></span>
<span data-ttu-id="88780-114">Jelzi, hogy az üzemi elemzések az információs üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="88780-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="88780-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="88780-115">-CollectWarnings</span></span>
<span data-ttu-id="88780-116">Jelzi, hogy a műveleti elemzések a figyelmeztető üzeneteket gyűjtik.</span><span class="sxs-lookup"><span data-stu-id="88780-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="88780-117">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="88780-117">-EventLogName</span></span>
<span data-ttu-id="88780-118">Az Eseménynapló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88780-118">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="88780-119">-Force</span><span class="sxs-lookup"><span data-stu-id="88780-119">-Force</span></span>
<span data-ttu-id="88780-120">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="88780-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88780-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="88780-121">-Name</span></span>
<span data-ttu-id="88780-122">Az adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88780-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="88780-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88780-123">-ResourceGroupName</span></span>
<span data-ttu-id="88780-124">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="88780-124">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="88780-125">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="88780-125">-Workspace</span></span>
<span data-ttu-id="88780-126">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="88780-126">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88780-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88780-127">-WorkspaceName</span></span>
<span data-ttu-id="88780-128">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="88780-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88780-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="88780-129">-Confirm</span></span>
<span data-ttu-id="88780-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="88780-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88780-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88780-131">-WhatIf</span></span>
<span data-ttu-id="88780-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="88780-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88780-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88780-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88780-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88780-134">-DefaultProfile</span></span>
<span data-ttu-id="88780-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88780-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88780-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88780-136">CommonParameters</span></span>
<span data-ttu-id="88780-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="88780-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88780-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88780-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88780-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="88780-139">INPUTS</span></span>

### <span data-ttu-id="88780-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="88780-140">PSWorkspace</span></span>
<span data-ttu-id="88780-141">A "Munkaterület" paraméter elfogadja a "PSWorkspace" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="88780-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="88780-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88780-142">OUTPUTS</span></span>

### <span data-ttu-id="88780-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="88780-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="88780-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="88780-144">NOTES</span></span>

## <span data-ttu-id="88780-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88780-145">RELATED LINKS</span></span>

