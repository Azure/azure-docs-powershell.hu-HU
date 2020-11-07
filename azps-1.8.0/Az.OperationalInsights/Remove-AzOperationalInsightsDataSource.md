---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: d8ec5eed1b6c955720822e28bf54da68e9aefcac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669839"
---
# <span data-ttu-id="2d6ea-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2d6ea-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="2d6ea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6ea-103">Törli az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-103">Deletes a data source.</span></span>

## <span data-ttu-id="2d6ea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d6ea-104">SYNTAX</span></span>

### <span data-ttu-id="2d6ea-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d6ea-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d6ea-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2d6ea-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d6ea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d6ea-107">DESCRIPTION</span></span>
<span data-ttu-id="2d6ea-108">A **Remove-AzOperationalInsightsDataSource** parancsmag törli az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="2d6ea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2d6ea-109">EXAMPLES</span></span>

## <span data-ttu-id="2d6ea-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d6ea-110">PARAMETERS</span></span>

### <span data-ttu-id="2d6ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d6ea-111">-DefaultProfile</span></span>
<span data-ttu-id="2d6ea-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d6ea-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d6ea-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2d6ea-113">-Force</span></span>
<span data-ttu-id="2d6ea-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d6ea-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d6ea-115">-Name</span></span>
<span data-ttu-id="2d6ea-116">A törlendő adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="2d6ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d6ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d6ea-118">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="2d6ea-119">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="2d6ea-119">-Workspace</span></span>
<span data-ttu-id="2d6ea-120">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d6ea-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2d6ea-121">-WorkspaceName</span></span>
<span data-ttu-id="2d6ea-122">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2d6ea-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d6ea-123">-Confirm</span></span>
<span data-ttu-id="2d6ea-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d6ea-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d6ea-125">-WhatIf</span></span>
<span data-ttu-id="2d6ea-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d6ea-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d6ea-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d6ea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6ea-128">CommonParameters</span></span>
<span data-ttu-id="2d6ea-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d6ea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6ea-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d6ea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6ea-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d6ea-131">INPUTS</span></span>

### <span data-ttu-id="2d6ea-132">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2d6ea-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2d6ea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2d6ea-133">System.String</span></span>

## <span data-ttu-id="2d6ea-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d6ea-134">OUTPUTS</span></span>

### <span data-ttu-id="2d6ea-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="2d6ea-135">System.Void</span></span>

## <span data-ttu-id="2d6ea-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d6ea-136">NOTES</span></span>
* <span data-ttu-id="2d6ea-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="2d6ea-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="2d6ea-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d6ea-138">RELATED LINKS</span></span>

[<span data-ttu-id="2d6ea-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2d6ea-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="2d6ea-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2d6ea-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


