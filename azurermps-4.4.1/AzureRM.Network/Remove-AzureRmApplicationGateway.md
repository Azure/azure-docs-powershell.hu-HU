---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: cd4824b73aa7fe7a80a3c4bccba37445a85c2c22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493421"
---
# <span data-ttu-id="2c6f8-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c6f8-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="2c6f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c6f8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6f8-103">Egy alkalmazás átjárójának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c6f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c6f8-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c6f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c6f8-105">DESCRIPTION</span></span>
<span data-ttu-id="2c6f8-106">A **Remove-AzureRmApplicationGateway** parancsmag eltávolítja az alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="2c6f8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2c6f8-107">EXAMPLES</span></span>

### <span data-ttu-id="2c6f8-108">1. példa: meghatározott alkalmazásobjektum eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2c6f8-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2c6f8-109">Ez a parancs eltávolítja a ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoport erőforrás csoportjában.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="2c6f8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c6f8-110">PARAMETERS</span></span>

### <span data-ttu-id="2c6f8-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2c6f8-111">-Force</span></span>
<span data-ttu-id="2c6f8-112">Azt jelzi, hogy a parancsmag kikényszeríti az alkalmazás átjárójának törlését, függetlenül attól, hogy az erőforrások hozzá vannak-e rendelve.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-112">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="2c6f8-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c6f8-113">-Name</span></span>
<span data-ttu-id="2c6f8-114">Az eltávolítandó alkalmazás-átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-114">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="2c6f8-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c6f8-115">-PassThru</span></span>
<span data-ttu-id="2c6f8-116">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2c6f8-117">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c6f8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c6f8-118">-ResourceGroupName</span></span>
<span data-ttu-id="2c6f8-119">Annak az erőforráscsoport-névnek a nevét adja meg, amelyhez az alkalmazás-átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-119">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="2c6f8-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c6f8-120">-Confirm</span></span>
<span data-ttu-id="2c6f8-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c6f8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c6f8-122">-WhatIf</span></span>
<span data-ttu-id="2c6f8-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c6f8-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c6f8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6f8-125">-DefaultProfile</span></span>
<span data-ttu-id="2c6f8-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c6f8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6f8-127">CommonParameters</span></span>
<span data-ttu-id="2c6f8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c6f8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6f8-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c6f8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6f8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c6f8-130">INPUTS</span></span>

## <span data-ttu-id="2c6f8-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c6f8-131">OUTPUTS</span></span>

### <span data-ttu-id="2c6f8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2c6f8-132">System.String</span></span>

## <span data-ttu-id="2c6f8-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c6f8-133">NOTES</span></span>

## <span data-ttu-id="2c6f8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c6f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="2c6f8-135">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c6f8-135">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


