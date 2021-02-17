---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 2e7240f607d2c9ed426c35f9427452640ceec84f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399345"
---
# <span data-ttu-id="254a3-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="254a3-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="254a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="254a3-102">SYNOPSIS</span></span>
<span data-ttu-id="254a3-103">Eltávolít egy műveletcsoportot.</span><span class="sxs-lookup"><span data-stu-id="254a3-103">Removes an action group.</span></span>

## <span data-ttu-id="254a3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="254a3-104">SYNTAX</span></span>

### <span data-ttu-id="254a3-105">ByPropertyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="254a3-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="254a3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="254a3-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="254a3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="254a3-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="254a3-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="254a3-108">DESCRIPTION</span></span>
<span data-ttu-id="254a3-109">Az **Remove-AzActionGroup** parancsmag eltávolít egy műveletcsoportot.</span><span class="sxs-lookup"><span data-stu-id="254a3-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="254a3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="254a3-110">EXAMPLES</span></span>

### <span data-ttu-id="254a3-111">1. példa: Műveletcsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="254a3-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="254a3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="254a3-112">PARAMETERS</span></span>

### <span data-ttu-id="254a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254a3-113">-DefaultProfile</span></span>
<span data-ttu-id="254a3-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="254a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="254a3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="254a3-115">-InputObject</span></span>
<span data-ttu-id="254a3-116">A műveletcsoport-erőforrás</span><span class="sxs-lookup"><span data-stu-id="254a3-116">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="254a3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="254a3-117">-Name</span></span>
<span data-ttu-id="254a3-118">A műveletcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="254a3-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="254a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="254a3-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="254a3-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254a3-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="254a3-121">-ResourceId</span></span>
<span data-ttu-id="254a3-122">Az i erőforrás</span><span class="sxs-lookup"><span data-stu-id="254a3-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254a3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="254a3-123">-Confirm</span></span>
<span data-ttu-id="254a3-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="254a3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="254a3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="254a3-125">-WhatIf</span></span>
<span data-ttu-id="254a3-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="254a3-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="254a3-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="254a3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="254a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254a3-128">CommonParameters</span></span>
<span data-ttu-id="254a3-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254a3-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="254a3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254a3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="254a3-131">INPUTS</span></span>

### <span data-ttu-id="254a3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="254a3-132">System.String</span></span>

### <span data-ttu-id="254a3-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="254a3-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="254a3-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="254a3-134">OUTPUTS</span></span>

### <span data-ttu-id="254a3-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="254a3-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="254a3-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="254a3-136">NOTES</span></span>

## <span data-ttu-id="254a3-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="254a3-137">RELATED LINKS</span></span>

<span data-ttu-id="254a3-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="254a3-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)</span></span>

