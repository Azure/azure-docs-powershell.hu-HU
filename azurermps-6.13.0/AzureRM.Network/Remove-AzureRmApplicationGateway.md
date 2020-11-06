---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: c7ce5872338b9fd3b7741f341d661d09c2eef16a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494041"
---
# <span data-ttu-id="9c0fc-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c0fc-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="9c0fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="9c0fc-103">Egy alkalmazás átjárójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c0fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c0fc-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c0fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c0fc-105">DESCRIPTION</span></span>
<span data-ttu-id="9c0fc-106">A **Remove-AzureRmApplicationGateway** parancsmag eltávolítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="9c0fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9c0fc-107">EXAMPLES</span></span>

### <span data-ttu-id="9c0fc-108">1. példa: meghatározott alkalmazásobjektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9c0fc-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9c0fc-109">Ez a parancs eltávolítja a ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoport erőforrás csoportjában.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="9c0fc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c0fc-110">PARAMETERS</span></span>

### <span data-ttu-id="9c0fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c0fc-111">-DefaultProfile</span></span>
<span data-ttu-id="9c0fc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c0fc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9c0fc-113">-Force</span></span>
<span data-ttu-id="9c0fc-114">Azt jelzi, hogy a parancsmag kikényszeríti az alkalmazás átjárójának törlését, függetlenül attól, hogy az erőforrások hozzá vannak-e rendelve.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="9c0fc-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c0fc-115">-Name</span></span>
<span data-ttu-id="9c0fc-116">Az eltávolítandó alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="9c0fc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c0fc-117">-PassThru</span></span>
<span data-ttu-id="9c0fc-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c0fc-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c0fc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c0fc-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c0fc-121">Annak az erőforráscsoport-névnek a nevét adja meg, amelyhez az alkalmazás-átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="9c0fc-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9c0fc-122">-Confirm</span></span>
<span data-ttu-id="9c0fc-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c0fc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c0fc-124">-WhatIf</span></span>
<span data-ttu-id="9c0fc-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c0fc-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9c0fc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c0fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c0fc-127">CommonParameters</span></span>
<span data-ttu-id="9c0fc-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c0fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c0fc-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c0fc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c0fc-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c0fc-130">INPUTS</span></span>

### <span data-ttu-id="9c0fc-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9c0fc-131">System.String</span></span>

### <span data-ttu-id="9c0fc-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9c0fc-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9c0fc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c0fc-133">OUTPUTS</span></span>

### <span data-ttu-id="9c0fc-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c0fc-134">System.Boolean</span></span>

## <span data-ttu-id="9c0fc-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c0fc-135">NOTES</span></span>

## <span data-ttu-id="9c0fc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c0fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="9c0fc-137">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9c0fc-137">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


