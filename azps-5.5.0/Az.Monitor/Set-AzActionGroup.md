---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: b10aad8cdf480dd567b0646fb3befa95fb32bf72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159403"
---
# <span data-ttu-id="0ca4a-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="0ca4a-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="0ca4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ca4a-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca4a-103">Létrehoz egy újat, vagy frissíti egy meglévő műveletcsoportot.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="0ca4a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ca4a-104">SYNTAX</span></span>

### <span data-ttu-id="0ca4a-105">ByPropertyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ca4a-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca4a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ca4a-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ca4a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0ca4a-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ca4a-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ca4a-108">DESCRIPTION</span></span>
<span data-ttu-id="0ca4a-109">A **Set-AzActionGroup** parancsmag létrehoz egy újat, vagy frissíti egy meglévő műveletcsoportot.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="0ca4a-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ca4a-110">EXAMPLES</span></span>

### <span data-ttu-id="0ca4a-111">1. példa: Műveletcsoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="0ca4a-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="0ca4a-112">Az első két parancs két fogadót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="0ca4a-113">Az utolsó parancs létrehoz egy műveletcsoportot a két fogadóval együtt.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="0ca4a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ca4a-114">PARAMETERS</span></span>

### <span data-ttu-id="0ca4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca4a-115">-DefaultProfile</span></span>
<span data-ttu-id="0ca4a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ca4a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ca4a-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="0ca4a-117">-DisableGroup</span></span>
<span data-ttu-id="0ca4a-118">Letiltja a műveletcsoportot.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca4a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ca4a-119">-InputObject</span></span>
<span data-ttu-id="0ca4a-120">A műveletcsoport-erőforrás</span><span class="sxs-lookup"><span data-stu-id="0ca4a-120">The action group resource</span></span>

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

### <span data-ttu-id="0ca4a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0ca4a-121">-Name</span></span>
<span data-ttu-id="0ca4a-122">A műveletcsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-122">The name of the action group.</span></span>

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

### <span data-ttu-id="0ca4a-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="0ca4a-123">-Receiver</span></span>
<span data-ttu-id="0ca4a-124">A műveletcsoport fogadóinak listája.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca4a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca4a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ca4a-126">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="0ca4a-126">The resource group nam</span></span>

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

### <span data-ttu-id="0ca4a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ca4a-127">-ResourceId</span></span>
<span data-ttu-id="0ca4a-128">Az i erőforrás</span><span class="sxs-lookup"><span data-stu-id="0ca4a-128">The resource i</span></span>

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

### <span data-ttu-id="0ca4a-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="0ca4a-129">-ShortName</span></span>
<span data-ttu-id="0ca4a-130">A műveletcsoport rövid neve.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca4a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ca4a-131">-Tag</span></span>
<span data-ttu-id="0ca4a-132">A műveletcsoport-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="0ca4a-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ca4a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ca4a-133">-Confirm</span></span>
<span data-ttu-id="0ca4a-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca4a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca4a-135">-WhatIf</span></span>
<span data-ttu-id="0ca4a-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ca4a-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ca4a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca4a-138">CommonParameters</span></span>
<span data-ttu-id="0ca4a-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ca4a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca4a-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ca4a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca4a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ca4a-141">INPUTS</span></span>

### <span data-ttu-id="0ca4a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0ca4a-142">System.String</span></span>

### <span data-ttu-id="0ca4a-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0ca4a-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0ca4a-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0ca4a-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0ca4a-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0ca4a-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0ca4a-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="0ca4a-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="0ca4a-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ca4a-147">OUTPUTS</span></span>

### <span data-ttu-id="0ca4a-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="0ca4a-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="0ca4a-149">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ca4a-149">NOTES</span></span>

## <span data-ttu-id="0ca4a-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ca4a-150">RELATED LINKS</span></span>

<span data-ttu-id="0ca4a-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="0ca4a-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
