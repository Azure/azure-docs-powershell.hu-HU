---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159034"
---
# <span data-ttu-id="06651-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06651-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="06651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06651-102">SYNOPSIS</span></span>
<span data-ttu-id="06651-103">Eltávolít egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="06651-103">Removes an application gateway.</span></span>

## <span data-ttu-id="06651-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="06651-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06651-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="06651-105">DESCRIPTION</span></span>
<span data-ttu-id="06651-106">A **Remove-AzApplicationGateway** parancsmag eltávolít egy alkalmazás-átjárót.</span><span class="sxs-lookup"><span data-stu-id="06651-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="06651-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="06651-107">EXAMPLES</span></span>

### <span data-ttu-id="06651-108">1. példa: Adott alkalmazás átjáró eltávolítása</span><span class="sxs-lookup"><span data-stu-id="06651-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="06651-109">Ez a parancs eltávolítja az ApplicationGateway01 nevű alkalmazás-átjárót az ResourceGroup01 nevű erőforráscsoportból.</span><span class="sxs-lookup"><span data-stu-id="06651-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="06651-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06651-110">PARAMETERS</span></span>

### <span data-ttu-id="06651-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06651-111">-DefaultProfile</span></span>
<span data-ttu-id="06651-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="06651-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06651-113">-Force</span><span class="sxs-lookup"><span data-stu-id="06651-113">-Force</span></span>
<span data-ttu-id="06651-114">Azt jelzi, hogy a parancsmag az alkalmazás-átjáró törlését kényszeríti függetlenül attól, hogy erőforrások vannak-e hozzá rendelve.</span><span class="sxs-lookup"><span data-stu-id="06651-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="06651-115">-Name</span><span class="sxs-lookup"><span data-stu-id="06651-115">-Name</span></span>
<span data-ttu-id="06651-116">Az eltávolítható alkalmazás átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06651-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="06651-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06651-117">-PassThru</span></span>
<span data-ttu-id="06651-118">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="06651-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06651-119">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="06651-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06651-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06651-120">-ResourceGroupName</span></span>
<span data-ttu-id="06651-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az alkalmazás-átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="06651-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="06651-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06651-122">-Confirm</span></span>
<span data-ttu-id="06651-123">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="06651-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06651-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06651-124">-WhatIf</span></span>
<span data-ttu-id="06651-125">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="06651-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06651-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06651-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06651-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06651-127">CommonParameters</span></span>
<span data-ttu-id="06651-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06651-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06651-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06651-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06651-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06651-130">INPUTS</span></span>

### <span data-ttu-id="06651-131">System.String</span><span class="sxs-lookup"><span data-stu-id="06651-131">System.String</span></span>

### <span data-ttu-id="06651-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="06651-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="06651-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06651-133">OUTPUTS</span></span>

### <span data-ttu-id="06651-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06651-134">System.Boolean</span></span>

## <span data-ttu-id="06651-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="06651-135">NOTES</span></span>

## <span data-ttu-id="06651-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06651-136">RELATED LINKS</span></span>

[<span data-ttu-id="06651-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06651-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


