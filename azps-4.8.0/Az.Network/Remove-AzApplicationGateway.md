---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184350"
---
# <span data-ttu-id="3bc2d-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3bc2d-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="3bc2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bc2d-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc2d-103">Egy alkalmazás átjárójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-103">Removes an application gateway.</span></span>

## <span data-ttu-id="3bc2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bc2d-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bc2d-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc2d-106">A **Remove-AzApplicationGateway** parancsmag eltávolítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="3bc2d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3bc2d-107">EXAMPLES</span></span>

### <span data-ttu-id="3bc2d-108">1. példa: meghatározott alkalmazásobjektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3bc2d-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3bc2d-109">Ez a parancs eltávolítja a ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoport erőforrás csoportjában.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3bc2d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bc2d-110">PARAMETERS</span></span>

### <span data-ttu-id="3bc2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc2d-111">-DefaultProfile</span></span>
<span data-ttu-id="3bc2d-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bc2d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3bc2d-113">-Force</span></span>
<span data-ttu-id="3bc2d-114">Azt jelzi, hogy a parancsmag kikényszeríti az alkalmazás átjárójának törlését, függetlenül attól, hogy az erőforrások hozzá vannak-e rendelve.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="3bc2d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3bc2d-115">-Name</span></span>
<span data-ttu-id="3bc2d-116">Az eltávolítandó alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc2d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bc2d-117">-PassThru</span></span>
<span data-ttu-id="3bc2d-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3bc2d-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3bc2d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc2d-120">-ResourceGroupName</span></span>
<span data-ttu-id="3bc2d-121">Annak az erőforráscsoport-névnek a nevét adja meg, amelyhez az alkalmazás-átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc2d-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3bc2d-122">-Confirm</span></span>
<span data-ttu-id="3bc2d-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc2d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc2d-124">-WhatIf</span></span>
<span data-ttu-id="3bc2d-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc2d-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bc2d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc2d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc2d-127">CommonParameters</span></span>
<span data-ttu-id="3bc2d-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bc2d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc2d-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bc2d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc2d-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bc2d-130">INPUTS</span></span>

### <span data-ttu-id="3bc2d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc2d-131">System.String</span></span>

### <span data-ttu-id="3bc2d-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3bc2d-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3bc2d-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bc2d-133">OUTPUTS</span></span>

### <span data-ttu-id="3bc2d-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3bc2d-134">System.Boolean</span></span>

## <span data-ttu-id="3bc2d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bc2d-135">NOTES</span></span>

## <span data-ttu-id="3bc2d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bc2d-136">RELATED LINKS</span></span>

[<span data-ttu-id="3bc2d-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3bc2d-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


