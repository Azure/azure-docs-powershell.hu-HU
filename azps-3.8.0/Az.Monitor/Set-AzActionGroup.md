---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: bcec58094fc124d3dd49fc2536a9427ed72d07a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845101"
---
# <span data-ttu-id="8a87e-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8a87e-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="8a87e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a87e-102">SYNOPSIS</span></span>
<span data-ttu-id="8a87e-103">Új vagy frissített meglévő műveleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="8a87e-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="8a87e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a87e-104">SYNTAX</span></span>

### <span data-ttu-id="8a87e-105">ByPropertyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a87e-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a87e-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a87e-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a87e-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8a87e-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a87e-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a87e-108">DESCRIPTION</span></span>
<span data-ttu-id="8a87e-109">A **set-AzActionGroup** parancsmag új vagy frissített meglévő műveleti csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8a87e-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="8a87e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8a87e-110">EXAMPLES</span></span>

### <span data-ttu-id="8a87e-111">Példa 1: műveleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="8a87e-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="8a87e-112">Az első két parancs két vevőegységet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8a87e-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="8a87e-113">A végleges parancs létrehoz egy műveleti csoportot, benne a két vevőegységet is.</span><span class="sxs-lookup"><span data-stu-id="8a87e-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="8a87e-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a87e-114">PARAMETERS</span></span>

### <span data-ttu-id="8a87e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a87e-115">-DefaultProfile</span></span>
<span data-ttu-id="8a87e-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8a87e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a87e-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="8a87e-117">-DisableGroup</span></span>
<span data-ttu-id="8a87e-118">Letiltja a műveleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="8a87e-118">Disables the action group.</span></span>

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

### <span data-ttu-id="8a87e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a87e-119">-InputObject</span></span>
<span data-ttu-id="8a87e-120">A műveleti csoport erőforrás</span><span class="sxs-lookup"><span data-stu-id="8a87e-120">The action group resource</span></span>

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

### <span data-ttu-id="8a87e-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a87e-121">-Name</span></span>
<span data-ttu-id="8a87e-122">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8a87e-122">The name of the action group.</span></span>

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

### <span data-ttu-id="8a87e-123">-Vevőkészülék</span><span class="sxs-lookup"><span data-stu-id="8a87e-123">-Receiver</span></span>
<span data-ttu-id="8a87e-124">A műveleti csoport fogadóinak listája.</span><span class="sxs-lookup"><span data-stu-id="8a87e-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="8a87e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a87e-125">-ResourceGroupName</span></span>
<span data-ttu-id="8a87e-126">A Nam erőforrás csoport</span><span class="sxs-lookup"><span data-stu-id="8a87e-126">The resource group nam</span></span>

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

### <span data-ttu-id="8a87e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a87e-127">-ResourceId</span></span>
<span data-ttu-id="8a87e-128">Az erőforrás i</span><span class="sxs-lookup"><span data-stu-id="8a87e-128">The resource i</span></span>

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

### <span data-ttu-id="8a87e-129">-Rövid névvel</span><span class="sxs-lookup"><span data-stu-id="8a87e-129">-ShortName</span></span>
<span data-ttu-id="8a87e-130">A műveleti csoport rövid neve.</span><span class="sxs-lookup"><span data-stu-id="8a87e-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="8a87e-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="8a87e-131">-Tag</span></span>
<span data-ttu-id="8a87e-132">A Művelettípus-erőforrás címkéi</span><span class="sxs-lookup"><span data-stu-id="8a87e-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="8a87e-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8a87e-133">-Confirm</span></span>
<span data-ttu-id="8a87e-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8a87e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a87e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a87e-135">-WhatIf</span></span>
<span data-ttu-id="8a87e-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8a87e-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a87e-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8a87e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a87e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a87e-138">CommonParameters</span></span>
<span data-ttu-id="8a87e-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a87e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a87e-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8a87e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a87e-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a87e-141">INPUTS</span></span>

### <span data-ttu-id="8a87e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="8a87e-142">System.String</span></span>

### <span data-ttu-id="8a87e-143">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. parancsmagok. monitor, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8a87e-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8a87e-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8a87e-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8a87e-145">System. Collections. Generic. IDictionary ' 2 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e], [System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8a87e-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8a87e-146">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="8a87e-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="8a87e-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a87e-147">OUTPUTS</span></span>

### <span data-ttu-id="8a87e-148">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="8a87e-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="8a87e-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a87e-149">NOTES</span></span>

## <span data-ttu-id="8a87e-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a87e-150">RELATED LINKS</span></span>

<span data-ttu-id="8a87e-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Új – AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="8a87e-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
