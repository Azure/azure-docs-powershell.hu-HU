---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: d9dc64124dd4840227b692e2ef21842a19b4adeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931681"
---
# <span data-ttu-id="6d3ab-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="6d3ab-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="6d3ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3ab-103">Adatkapcsolat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6d3ab-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="6d3ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d3ab-104">SYNTAX</span></span>

### <span data-ttu-id="6d3ab-105">DataConnectorId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6d3ab-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d3ab-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6d3ab-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d3ab-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d3ab-107">DESCRIPTION</span></span>
<span data-ttu-id="6d3ab-108">A **Remove-AzSentinelDataConnector** parancsmag véglegesen töröl egy adatösszekötőt egy adott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="6d3ab-109">A **DataConnector-objektumokat** átadhatja a folyamat műveleti jelével, vagy megadhatja a szükséges paramétereket.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="6d3ab-110">A Confirm paraméter és a Windows PowerShell $ConfirmPreference szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6d3ab-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d3ab-111">EXAMPLES</span></span>

### <span data-ttu-id="6d3ab-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6d3ab-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="6d3ab-113">Ez a parancs eltávolítja az Adatösszekötőt a munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="6d3ab-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d3ab-114">PARAMETERS</span></span>

### <span data-ttu-id="6d3ab-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="6d3ab-115">-DataConnectorId</span></span>
<span data-ttu-id="6d3ab-116">Adatkapcsolat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-116">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ab-117">-DefaultProfile</span></span>
<span data-ttu-id="6d3ab-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d3ab-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d3ab-119">-InputObject</span></span>
<span data-ttu-id="6d3ab-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ab-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d3ab-121">-PassThru</span></span>
<span data-ttu-id="6d3ab-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="6d3ab-122">PassThru</span></span>

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

### <span data-ttu-id="6d3ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d3ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d3ab-124">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ab-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6d3ab-125">-WorkspaceName</span></span>
<span data-ttu-id="6d3ab-126">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ab-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d3ab-127">-Confirm</span></span>
<span data-ttu-id="6d3ab-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ab-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d3ab-129">-WhatIf</span></span>
<span data-ttu-id="6d3ab-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d3ab-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3ab-132">CommonParameters</span></span>
<span data-ttu-id="6d3ab-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d3ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3ab-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d3ab-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3ab-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d3ab-135">INPUTS</span></span>

### <span data-ttu-id="6d3ab-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6d3ab-136">System.String</span></span>
### <span data-ttu-id="6d3ab-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="6d3ab-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="6d3ab-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d3ab-138">OUTPUTS</span></span>

### <span data-ttu-id="6d3ab-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="6d3ab-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="6d3ab-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d3ab-140">NOTES</span></span>

## <span data-ttu-id="6d3ab-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d3ab-141">RELATED LINKS</span></span>
