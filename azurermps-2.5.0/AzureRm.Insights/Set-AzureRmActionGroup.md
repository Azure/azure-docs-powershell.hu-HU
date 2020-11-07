---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 3f8b3ad20e9a80344227a28dd7cd1f2763cbaab4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848489"
---
# <span data-ttu-id="f4ebc-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="f4ebc-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="f4ebc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f4ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ebc-103">Új vagy frissített meglévő műveleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4ebc-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4ebc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f4ebc-104">SYNTAX</span></span>

### <span data-ttu-id="f4ebc-105">ByPropertyName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f4ebc-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ebc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ebc-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ebc-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f4ebc-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4ebc-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f4ebc-108">DESCRIPTION</span></span>
<span data-ttu-id="f4ebc-109">A **set-AzureRmActionGroup** parancsmag új vagy frissített meglévő műveleti csoportot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="f4ebc-110">Példák</span><span class="sxs-lookup"><span data-stu-id="f4ebc-110">EXAMPLES</span></span>

### <span data-ttu-id="f4ebc-111">Példa 1: műveleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="f4ebc-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="f4ebc-112">Az első két parancs két vevőegységet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="f4ebc-113">A végleges parancs létrehoz egy műveleti csoportot, benne a két vevőegységet is.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="f4ebc-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f4ebc-114">PARAMETERS</span></span>

### <span data-ttu-id="f4ebc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ebc-115">-DefaultProfile</span></span>
<span data-ttu-id="f4ebc-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f4ebc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4ebc-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="f4ebc-117">-DisableGroup</span></span>
<span data-ttu-id="f4ebc-118">Letiltja a műveleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-118">Disables the action group.</span></span>

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

### <span data-ttu-id="f4ebc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4ebc-119">-InputObject</span></span>
<span data-ttu-id="f4ebc-120">A műveleti csoport resourc</span><span class="sxs-lookup"><span data-stu-id="f4ebc-120">The action group resourc</span></span>

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

### <span data-ttu-id="f4ebc-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f4ebc-121">-Name</span></span>
<span data-ttu-id="f4ebc-122">A műveleti csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-122">The name of the action group.</span></span>

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

### <span data-ttu-id="f4ebc-123">-Vevőkészülék</span><span class="sxs-lookup"><span data-stu-id="f4ebc-123">-Receiver</span></span>
<span data-ttu-id="f4ebc-124">A műveleti csoport fogadóinak listája.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="f4ebc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ebc-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4ebc-126">A Nam erőforrás csoport</span><span class="sxs-lookup"><span data-stu-id="f4ebc-126">The resource group nam</span></span>

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

### <span data-ttu-id="f4ebc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4ebc-127">-ResourceId</span></span>
<span data-ttu-id="f4ebc-128">Az erőforrás i</span><span class="sxs-lookup"><span data-stu-id="f4ebc-128">The resource i</span></span>

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

### <span data-ttu-id="f4ebc-129">-Rövid névvel</span><span class="sxs-lookup"><span data-stu-id="f4ebc-129">-ShortName</span></span>
<span data-ttu-id="f4ebc-130">A műveleti csoport rövid neve.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="f4ebc-131">-Címke</span><span class="sxs-lookup"><span data-stu-id="f4ebc-131">-Tag</span></span>
<span data-ttu-id="f4ebc-132">A műveleti csoport resourc címkéi</span><span class="sxs-lookup"><span data-stu-id="f4ebc-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="f4ebc-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f4ebc-133">-Confirm</span></span>
<span data-ttu-id="f4ebc-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ebc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ebc-135">-WhatIf</span></span>
<span data-ttu-id="f4ebc-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4ebc-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f4ebc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ebc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ebc-138">CommonParameters</span></span>
<span data-ttu-id="f4ebc-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f4ebc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ebc-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4ebc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ebc-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4ebc-141">INPUTS</span></span>

### <span data-ttu-id="f4ebc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f4ebc-142">System.String</span></span>

### <span data-ttu-id="f4ebc-143">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. commands. ininsights, Version = 5.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f4ebc-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f4ebc-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4ebc-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f4ebc-145">System. Collections. Generic. IDictionary ' 2 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089], [System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f4ebc-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f4ebc-146">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="f4ebc-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="f4ebc-147">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4ebc-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f4ebc-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f4ebc-148">OUTPUTS</span></span>

### <span data-ttu-id="f4ebc-149">Microsoft. Azure. commands. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="f4ebc-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="f4ebc-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f4ebc-150">NOTES</span></span>

## <span data-ttu-id="f4ebc-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f4ebc-151">RELATED LINKS</span></span>

<span data-ttu-id="f4ebc-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Új – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="f4ebc-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
