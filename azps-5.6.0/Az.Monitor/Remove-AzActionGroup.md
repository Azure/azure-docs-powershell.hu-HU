---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: 50d9e49319f8171ea8c0fea93e9474bd175b417f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928586"
---
# <span data-ttu-id="1e38a-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1e38a-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="1e38a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e38a-102">SYNOPSIS</span></span>
<span data-ttu-id="1e38a-103">Eltávolít egy műveletcsoportot.</span><span class="sxs-lookup"><span data-stu-id="1e38a-103">Removes an action group.</span></span>

## <span data-ttu-id="1e38a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1e38a-104">SYNTAX</span></span>

### <span data-ttu-id="1e38a-105">ByPropertyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1e38a-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e38a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e38a-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e38a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e38a-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e38a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1e38a-108">DESCRIPTION</span></span>
<span data-ttu-id="1e38a-109">Az **Remove-AzActionGroup** parancsmag eltávolít egy műveletcsoportot.</span><span class="sxs-lookup"><span data-stu-id="1e38a-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="1e38a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1e38a-110">EXAMPLES</span></span>

### <span data-ttu-id="1e38a-111">1. példa: Műveletcsoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1e38a-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="1e38a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e38a-112">PARAMETERS</span></span>

### <span data-ttu-id="1e38a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e38a-113">-DefaultProfile</span></span>
<span data-ttu-id="1e38a-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1e38a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e38a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e38a-115">-InputObject</span></span>
<span data-ttu-id="1e38a-116">A műveletcsoport-erőforrás</span><span class="sxs-lookup"><span data-stu-id="1e38a-116">The action group resource</span></span>

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

### <span data-ttu-id="1e38a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1e38a-117">-Name</span></span>
<span data-ttu-id="1e38a-118">A műveletcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e38a-118">The name of the action group.</span></span>

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

### <span data-ttu-id="1e38a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e38a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1e38a-120">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="1e38a-120">The resource group nam</span></span>

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

### <span data-ttu-id="1e38a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e38a-121">-ResourceId</span></span>
<span data-ttu-id="1e38a-122">Az i erőforrás</span><span class="sxs-lookup"><span data-stu-id="1e38a-122">The resource i</span></span>

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

### <span data-ttu-id="1e38a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e38a-123">-Confirm</span></span>
<span data-ttu-id="1e38a-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1e38a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e38a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e38a-125">-WhatIf</span></span>
<span data-ttu-id="1e38a-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1e38a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e38a-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1e38a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e38a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e38a-128">CommonParameters</span></span>
<span data-ttu-id="1e38a-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e38a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e38a-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e38a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e38a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e38a-131">INPUTS</span></span>

### <span data-ttu-id="1e38a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1e38a-132">System.String</span></span>

### <span data-ttu-id="1e38a-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="1e38a-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="1e38a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e38a-134">OUTPUTS</span></span>

### <span data-ttu-id="1e38a-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1e38a-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1e38a-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1e38a-136">NOTES</span></span>

## <span data-ttu-id="1e38a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e38a-137">RELATED LINKS</span></span>

<span data-ttu-id="1e38a-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="1e38a-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
