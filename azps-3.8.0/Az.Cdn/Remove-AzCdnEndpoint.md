---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012833"
---
# <span data-ttu-id="b972b-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b972b-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="b972b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b972b-102">SYNOPSIS</span></span>
<span data-ttu-id="b972b-103">Egy CDN-végpont eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="b972b-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="b972b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b972b-104">SYNTAX</span></span>

### <span data-ttu-id="b972b-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b972b-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b972b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b972b-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b972b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b972b-107">DESCRIPTION</span></span>
<span data-ttu-id="b972b-108">A **Remove-AzCdnEndpoint** parancsmag eltávolítja az Azure Content Delivery Network (CDN) végpontját.</span><span class="sxs-lookup"><span data-stu-id="b972b-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="b972b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b972b-109">EXAMPLES</span></span>

## <span data-ttu-id="b972b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b972b-110">PARAMETERS</span></span>

### <span data-ttu-id="b972b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b972b-111">-CdnEndpoint</span></span>
<span data-ttu-id="b972b-112">A parancsmag által eltávolított végpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="b972b-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b972b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b972b-113">-DefaultProfile</span></span>
<span data-ttu-id="b972b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b972b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b972b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b972b-115">-EndpointName</span></span>
<span data-ttu-id="b972b-116">A parancsmag által eltávolított végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b972b-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b972b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b972b-117">-Force</span></span>
<span data-ttu-id="b972b-118">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="b972b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b972b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b972b-119">-PassThru</span></span>
<span data-ttu-id="b972b-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="b972b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b972b-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="b972b-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b972b-122">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="b972b-122">-ProfileName</span></span>
<span data-ttu-id="b972b-123">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="b972b-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b972b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b972b-124">-ResourceGroupName</span></span>
<span data-ttu-id="b972b-125">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="b972b-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b972b-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b972b-126">-Confirm</span></span>
<span data-ttu-id="b972b-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b972b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b972b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b972b-128">-WhatIf</span></span>
<span data-ttu-id="b972b-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b972b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b972b-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b972b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b972b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b972b-131">CommonParameters</span></span>
<span data-ttu-id="b972b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b972b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b972b-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b972b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b972b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b972b-134">INPUTS</span></span>

### <span data-ttu-id="b972b-135">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b972b-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="b972b-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b972b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b972b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b972b-137">OUTPUTS</span></span>

### <span data-ttu-id="b972b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b972b-138">System.Boolean</span></span>

## <span data-ttu-id="b972b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b972b-139">NOTES</span></span>

## <span data-ttu-id="b972b-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b972b-140">RELATED LINKS</span></span>

[<span data-ttu-id="b972b-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b972b-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="b972b-142">Új – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b972b-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="b972b-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b972b-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="b972b-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b972b-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="b972b-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b972b-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


