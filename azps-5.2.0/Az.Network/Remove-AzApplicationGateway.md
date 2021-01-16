---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345138"
---
# <span data-ttu-id="07bc1-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07bc1-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="07bc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="07bc1-103">Eltávolít egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="07bc1-103">Removes an application gateway.</span></span>

## <span data-ttu-id="07bc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="07bc1-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07bc1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="07bc1-105">DESCRIPTION</span></span>
<span data-ttu-id="07bc1-106">A **Remove-AzApplicationGateway** parancsmag eltávolít egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="07bc1-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="07bc1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="07bc1-107">EXAMPLES</span></span>

### <span data-ttu-id="07bc1-108">1. példa: Adott alkalmazás átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="07bc1-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="07bc1-109">Ez a parancs eltávolítja az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="07bc1-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="07bc1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07bc1-110">PARAMETERS</span></span>

### <span data-ttu-id="07bc1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bc1-111">-DefaultProfile</span></span>
<span data-ttu-id="07bc1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07bc1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07bc1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="07bc1-113">-Force</span></span>
<span data-ttu-id="07bc1-114">Azt jelzi, hogy a parancsmag az alkalmazás-átjáró törlését kényszeríti függetlenül attól, hogy erőforrások vannak-e hozzá rendelve.</span><span class="sxs-lookup"><span data-stu-id="07bc1-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="07bc1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="07bc1-115">-Name</span></span>
<span data-ttu-id="07bc1-116">Az eltávolítható alkalmazás átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="07bc1-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="07bc1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07bc1-117">-PassThru</span></span>
<span data-ttu-id="07bc1-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="07bc1-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="07bc1-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="07bc1-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="07bc1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bc1-120">-ResourceGroupName</span></span>
<span data-ttu-id="07bc1-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az alkalmazás-átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="07bc1-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="07bc1-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07bc1-122">-Confirm</span></span>
<span data-ttu-id="07bc1-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="07bc1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07bc1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07bc1-124">-WhatIf</span></span>
<span data-ttu-id="07bc1-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="07bc1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07bc1-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="07bc1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07bc1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bc1-127">CommonParameters</span></span>
<span data-ttu-id="07bc1-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07bc1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bc1-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bc1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bc1-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07bc1-130">INPUTS</span></span>

### <span data-ttu-id="07bc1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="07bc1-131">System.String</span></span>

### <span data-ttu-id="07bc1-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="07bc1-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="07bc1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07bc1-133">OUTPUTS</span></span>

### <span data-ttu-id="07bc1-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07bc1-134">System.Boolean</span></span>

## <span data-ttu-id="07bc1-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="07bc1-135">NOTES</span></span>

## <span data-ttu-id="07bc1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07bc1-136">RELATED LINKS</span></span>

[<span data-ttu-id="07bc1-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="07bc1-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


