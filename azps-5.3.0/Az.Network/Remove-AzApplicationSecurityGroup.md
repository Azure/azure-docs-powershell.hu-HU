---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385333"
---
# <span data-ttu-id="a9bfa-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a9bfa-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="a9bfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bfa-103">Eltávolít egy alkalmazásbiztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-103">Removes an application security group.</span></span>

## <span data-ttu-id="a9bfa-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9bfa-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9bfa-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="a9bfa-106">A **Remove-AzApplicationSecurityGroup** parancsmag eltávolít egy alkalmazásbiztonsági csoportot.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="a9bfa-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9bfa-107">EXAMPLES</span></span>

### <span data-ttu-id="a9bfa-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="a9bfa-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a9bfa-109">Ez a parancs törli a MyApplicationSecurityGrouo nevű alkalmazásbiztonsági csoportot a MyResourceGroup nevű erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a9bfa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9bfa-110">PARAMETERS</span></span>

### <span data-ttu-id="a9bfa-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9bfa-111">-AsJob</span></span>
<span data-ttu-id="a9bfa-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a9bfa-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9bfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bfa-113">-DefaultProfile</span></span>
<span data-ttu-id="a9bfa-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9bfa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a9bfa-115">-Force</span></span>
<span data-ttu-id="a9bfa-116">Ne kérjen megerősítést, ha erőforrást szeretne törölni</span><span class="sxs-lookup"><span data-stu-id="a9bfa-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="a9bfa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a9bfa-117">-Name</span></span>
<span data-ttu-id="a9bfa-118">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="a9bfa-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9bfa-119">-PassThru</span></span>
<span data-ttu-id="a9bfa-120">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a9bfa-121">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a9bfa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9bfa-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9bfa-123">Az alkalmazás biztonsági csoportjának erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="a9bfa-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9bfa-124">-Confirm</span></span>
<span data-ttu-id="a9bfa-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9bfa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9bfa-126">-WhatIf</span></span>
<span data-ttu-id="a9bfa-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9bfa-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9bfa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bfa-129">CommonParameters</span></span>
<span data-ttu-id="a9bfa-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9bfa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bfa-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9bfa-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bfa-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9bfa-132">INPUTS</span></span>

### <span data-ttu-id="a9bfa-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a9bfa-133">System.String</span></span>

## <span data-ttu-id="a9bfa-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9bfa-134">OUTPUTS</span></span>

### <span data-ttu-id="a9bfa-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a9bfa-135">System.Boolean</span></span>

## <span data-ttu-id="a9bfa-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9bfa-136">NOTES</span></span>

## <span data-ttu-id="a9bfa-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9bfa-137">RELATED LINKS</span></span>

[<span data-ttu-id="a9bfa-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a9bfa-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="a9bfa-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a9bfa-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
