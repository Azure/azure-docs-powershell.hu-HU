---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: 962c7d8f5120e0d6ae75d584edf261307bcefbee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837084"
---
# <span data-ttu-id="ec7ab-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec7ab-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="ec7ab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7ab-103">Nyilvános IP-előtag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ec7ab-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="ec7ab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec7ab-104">SYNTAX</span></span>

### <span data-ttu-id="ec7ab-105">RemoveByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ec7ab-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec7ab-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec7ab-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec7ab-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec7ab-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec7ab-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec7ab-108">DESCRIPTION</span></span>
<span data-ttu-id="ec7ab-109">A **Remove-AzPublicIpPrefix** parancsmag mindaddig eltávolítja az Azure nyilvános IP-előtagot, ameddig nincs kiosztott nyilvános IP-cím.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="ec7ab-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ec7ab-110">EXAMPLES</span></span>

### <span data-ttu-id="ec7ab-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec7ab-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="ec7ab-112">A $prefixName nevű nyilvános IP-előtag eltávolítása az erőforrás csoportból $rgName</span><span class="sxs-lookup"><span data-stu-id="ec7ab-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="ec7ab-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec7ab-113">PARAMETERS</span></span>

### <span data-ttu-id="ec7ab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec7ab-114">-AsJob</span></span>
<span data-ttu-id="ec7ab-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ec7ab-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec7ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7ab-116">-DefaultProfile</span></span>
<span data-ttu-id="ec7ab-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec7ab-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ec7ab-118">-Force</span></span>
<span data-ttu-id="ec7ab-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ec7ab-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec7ab-120">-InputObject</span></span>
<span data-ttu-id="ec7ab-121">PublicIpPrefix objektum</span><span class="sxs-lookup"><span data-stu-id="ec7ab-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7ab-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec7ab-122">-Name</span></span>
<span data-ttu-id="ec7ab-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7ab-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec7ab-124">-PassThru</span></span>
<span data-ttu-id="ec7ab-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ec7ab-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ec7ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec7ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec7ab-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7ab-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec7ab-129">-ResourceId</span></span>
<span data-ttu-id="ec7ab-130">Az eltávolítandó erőforrás resourceId</span><span class="sxs-lookup"><span data-stu-id="ec7ab-130">The resourceId for the resource to remove</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7ab-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ec7ab-131">-Confirm</span></span>
<span data-ttu-id="ec7ab-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec7ab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec7ab-133">-WhatIf</span></span>
<span data-ttu-id="ec7ab-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec7ab-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec7ab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec7ab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7ab-136">CommonParameters</span></span>
<span data-ttu-id="ec7ab-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec7ab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7ab-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec7ab-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7ab-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec7ab-139">INPUTS</span></span>

### <span data-ttu-id="ec7ab-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ec7ab-140">System.String</span></span>

### <span data-ttu-id="ec7ab-141">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec7ab-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="ec7ab-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec7ab-142">OUTPUTS</span></span>

### <span data-ttu-id="ec7ab-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec7ab-143">System.Boolean</span></span>

## <span data-ttu-id="ec7ab-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec7ab-144">NOTES</span></span>

## <span data-ttu-id="ec7ab-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec7ab-145">RELATED LINKS</span></span>

[<span data-ttu-id="ec7ab-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec7ab-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="ec7ab-147">Új – AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec7ab-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="ec7ab-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="ec7ab-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
