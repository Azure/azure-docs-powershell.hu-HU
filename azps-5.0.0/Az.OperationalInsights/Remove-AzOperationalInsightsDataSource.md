---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188082"
---
# <span data-ttu-id="13dc0-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="13dc0-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="13dc0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="13dc0-103">Törli az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="13dc0-103">Deletes a data source.</span></span>

## <span data-ttu-id="13dc0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13dc0-104">SYNTAX</span></span>

### <span data-ttu-id="13dc0-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13dc0-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13dc0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="13dc0-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13dc0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="13dc0-107">DESCRIPTION</span></span>
<span data-ttu-id="13dc0-108">A **Remove-AzOperationalInsightsDataSource** parancsmag törli az adatforrást.</span><span class="sxs-lookup"><span data-stu-id="13dc0-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="13dc0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="13dc0-109">EXAMPLES</span></span>

## <span data-ttu-id="13dc0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13dc0-110">PARAMETERS</span></span>

### <span data-ttu-id="13dc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13dc0-111">-DefaultProfile</span></span>
<span data-ttu-id="13dc0-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="13dc0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13dc0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="13dc0-113">-Force</span></span>
<span data-ttu-id="13dc0-114">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="13dc0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13dc0-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13dc0-115">-Name</span></span>
<span data-ttu-id="13dc0-116">A törlendő adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13dc0-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="13dc0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13dc0-117">-ResourceGroupName</span></span>
<span data-ttu-id="13dc0-118">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="13dc0-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="13dc0-119">-Munkaterület</span><span class="sxs-lookup"><span data-stu-id="13dc0-119">-Workspace</span></span>
<span data-ttu-id="13dc0-120">Itt adhatja meg azt a munkaterületet, amelyben ez a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="13dc0-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="13dc0-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="13dc0-121">-WorkspaceName</span></span>
<span data-ttu-id="13dc0-122">Annak a munkaterületnek a nevét adja meg, amelyben a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="13dc0-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="13dc0-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="13dc0-123">-Confirm</span></span>
<span data-ttu-id="13dc0-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="13dc0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13dc0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13dc0-125">-WhatIf</span></span>
<span data-ttu-id="13dc0-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="13dc0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13dc0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="13dc0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13dc0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13dc0-128">CommonParameters</span></span>
<span data-ttu-id="13dc0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13dc0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13dc0-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13dc0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13dc0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13dc0-131">INPUTS</span></span>

### <span data-ttu-id="13dc0-132">Microsoft. Azure. Command. OperationalInsights. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="13dc0-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="13dc0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="13dc0-133">System.String</span></span>

## <span data-ttu-id="13dc0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13dc0-134">OUTPUTS</span></span>

### <span data-ttu-id="13dc0-135">System. Void</span><span class="sxs-lookup"><span data-stu-id="13dc0-135">System.Void</span></span>

## <span data-ttu-id="13dc0-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13dc0-136">NOTES</span></span>
* <span data-ttu-id="13dc0-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, működési, betekintések</span><span class="sxs-lookup"><span data-stu-id="13dc0-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="13dc0-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13dc0-138">RELATED LINKS</span></span>

[<span data-ttu-id="13dc0-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="13dc0-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="13dc0-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="13dc0-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


