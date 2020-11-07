---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
ms.openlocfilehash: e361e4d3c4daec88ddb35fa7973b65f630dcc390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680041"
---
# <span data-ttu-id="4aa36-101">Remove-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4aa36-101">Remove-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="4aa36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4aa36-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa36-103">Nyilvános IP-előtag eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4aa36-103">Removes a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aa36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4aa36-104">SYNTAX</span></span>

### <span data-ttu-id="4aa36-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aa36-105">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa36-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aa36-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aa36-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aa36-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aa36-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4aa36-108">DESCRIPTION</span></span>
<span data-ttu-id="4aa36-109">A \* \* Remove-AzureRmPublicIpPrefix parancsmag az Azure nyilvános IP-előtagot mindaddig eltávolítja, amíg nincs kiosztott nyilvános IP-cím.</span><span class="sxs-lookup"><span data-stu-id="4aa36-109">The \*\*Remove-AzureRmPublicIpPrefix cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="4aa36-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4aa36-110">EXAMPLES</span></span>

### <span data-ttu-id="4aa36-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4aa36-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="4aa36-112">A $prefixName nevű nyilvános IP-előtag eltávolítása az erőforrás csoportból $rgName</span><span class="sxs-lookup"><span data-stu-id="4aa36-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="4aa36-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4aa36-113">PARAMETERS</span></span>

### <span data-ttu-id="4aa36-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4aa36-114">-AsJob</span></span>
<span data-ttu-id="4aa36-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4aa36-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa36-116">-DefaultProfile</span></span>
<span data-ttu-id="4aa36-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4aa36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4aa36-118">-Force</span></span>
<span data-ttu-id="4aa36-119">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4aa36-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4aa36-120">-InputObject</span></span>
<span data-ttu-id="4aa36-121">PublicIpPrefix objektum</span><span class="sxs-lookup"><span data-stu-id="4aa36-121">A PublicIpPrefix object</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4aa36-122">-Name</span></span>
<span data-ttu-id="4aa36-123">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="4aa36-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4aa36-124">-PassThru</span></span>
<span data-ttu-id="4aa36-125">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="4aa36-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4aa36-126">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="4aa36-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aa36-127">-ResourceGroupName</span></span>
<span data-ttu-id="4aa36-128">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4aa36-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4aa36-129">-ResourceId</span></span>
<span data-ttu-id="4aa36-130">Az eltávolítandó erőforrás resourceId</span><span class="sxs-lookup"><span data-stu-id="4aa36-130">The resourceId for the resource to remove</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4aa36-131">-Confirm</span></span>
<span data-ttu-id="4aa36-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4aa36-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aa36-133">-WhatIf</span></span>
<span data-ttu-id="4aa36-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4aa36-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aa36-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4aa36-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aa36-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa36-136">CommonParameters</span></span>
<span data-ttu-id="4aa36-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4aa36-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4aa36-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aa36-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa36-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aa36-139">INPUTS</span></span>

### <span data-ttu-id="4aa36-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4aa36-140">System.String</span></span>
<span data-ttu-id="4aa36-141">Microsoft. Azure. commands. Network. models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="4aa36-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="4aa36-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4aa36-142">OUTPUTS</span></span>

### <span data-ttu-id="4aa36-143">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="4aa36-143">System.Object</span></span>

## <span data-ttu-id="4aa36-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4aa36-144">NOTES</span></span>

## <span data-ttu-id="4aa36-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4aa36-145">RELATED LINKS</span></span>
