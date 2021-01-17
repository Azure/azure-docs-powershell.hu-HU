---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359168"
---
# <span data-ttu-id="cfd9e-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cfd9e-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="cfd9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfd9e-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd9e-103">Egy adatforrás törlése.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-103">Deletes a data source.</span></span>

## <span data-ttu-id="cfd9e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cfd9e-104">SYNTAX</span></span>

### <span data-ttu-id="cfd9e-105">ByWorkspaceName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cfd9e-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfd9e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cfd9e-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfd9e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cfd9e-107">DESCRIPTION</span></span>
<span data-ttu-id="cfd9e-108">A **Remove-AzOperationalInsightsDataSource** parancsmag töröl egy adatforrást.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="cfd9e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cfd9e-109">EXAMPLES</span></span>

## <span data-ttu-id="cfd9e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfd9e-110">PARAMETERS</span></span>

### <span data-ttu-id="cfd9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfd9e-111">-DefaultProfile</span></span>
<span data-ttu-id="cfd9e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cfd9e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfd9e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cfd9e-113">-Force</span></span>
<span data-ttu-id="cfd9e-114">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cfd9e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="cfd9e-115">-Name</span></span>
<span data-ttu-id="cfd9e-116">A törölni kívánt adatforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="cfd9e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd9e-117">-ResourceGroupName</span></span>
<span data-ttu-id="cfd9e-118">A számítógépeket tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-118">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="cfd9e-119">-Workspace</span><span class="sxs-lookup"><span data-stu-id="cfd9e-119">-Workspace</span></span>
<span data-ttu-id="cfd9e-120">Azt a munkaterületet adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-120">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cfd9e-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cfd9e-121">-WorkspaceName</span></span>
<span data-ttu-id="cfd9e-122">Annak a munkaterületnek a nevét adja meg, amelyen a parancsmag működik.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cfd9e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfd9e-123">-Confirm</span></span>
<span data-ttu-id="cfd9e-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd9e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd9e-125">-WhatIf</span></span>
<span data-ttu-id="cfd9e-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfd9e-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfd9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd9e-128">CommonParameters</span></span>
<span data-ttu-id="cfd9e-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfd9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd9e-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd9e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd9e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfd9e-131">INPUTS</span></span>

### <span data-ttu-id="cfd9e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cfd9e-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="cfd9e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="cfd9e-133">System.String</span></span>

## <span data-ttu-id="cfd9e-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfd9e-134">OUTPUTS</span></span>

### <span data-ttu-id="cfd9e-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="cfd9e-135">System.Void</span></span>

## <span data-ttu-id="cfd9e-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cfd9e-136">NOTES</span></span>
* <span data-ttu-id="cfd9e-137">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, műveleti, betekintések</span><span class="sxs-lookup"><span data-stu-id="cfd9e-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cfd9e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfd9e-138">RELATED LINKS</span></span>

[<span data-ttu-id="cfd9e-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cfd9e-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="cfd9e-140">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="cfd9e-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


