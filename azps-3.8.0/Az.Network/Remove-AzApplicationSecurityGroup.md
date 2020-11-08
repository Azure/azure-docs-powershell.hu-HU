---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014084"
---
# <span data-ttu-id="077bd-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="077bd-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="077bd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="077bd-102">SYNOPSIS</span></span>
<span data-ttu-id="077bd-103">Egy alkalmazás biztonsági csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="077bd-103">Removes an application security group.</span></span>

## <span data-ttu-id="077bd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="077bd-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="077bd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="077bd-105">DESCRIPTION</span></span>
<span data-ttu-id="077bd-106">A **Remove-AzApplicationSecurityGroup** parancsmag eltávolítja az alkalmazások biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="077bd-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="077bd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="077bd-107">EXAMPLES</span></span>

### <span data-ttu-id="077bd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="077bd-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="077bd-109">Ez a parancs törli a MyApplicationSecurityGrouo nevű alkalmazás biztonsági csoportját a MyResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="077bd-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="077bd-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="077bd-110">PARAMETERS</span></span>

### <span data-ttu-id="077bd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="077bd-111">-AsJob</span></span>
<span data-ttu-id="077bd-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="077bd-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="077bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077bd-113">-DefaultProfile</span></span>
<span data-ttu-id="077bd-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="077bd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="077bd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="077bd-115">-Force</span></span>
<span data-ttu-id="077bd-116">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="077bd-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="077bd-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="077bd-117">-Name</span></span>
<span data-ttu-id="077bd-118">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="077bd-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="077bd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="077bd-119">-PassThru</span></span>
<span data-ttu-id="077bd-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="077bd-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="077bd-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="077bd-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="077bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="077bd-123">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="077bd-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="077bd-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="077bd-124">-Confirm</span></span>
<span data-ttu-id="077bd-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="077bd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="077bd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077bd-126">-WhatIf</span></span>
<span data-ttu-id="077bd-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="077bd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="077bd-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="077bd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="077bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077bd-129">CommonParameters</span></span>
<span data-ttu-id="077bd-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="077bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077bd-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="077bd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077bd-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="077bd-132">INPUTS</span></span>

### <span data-ttu-id="077bd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="077bd-133">System.String</span></span>

## <span data-ttu-id="077bd-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="077bd-134">OUTPUTS</span></span>

### <span data-ttu-id="077bd-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="077bd-135">System.Boolean</span></span>

## <span data-ttu-id="077bd-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="077bd-136">NOTES</span></span>

## <span data-ttu-id="077bd-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="077bd-137">RELATED LINKS</span></span>

[<span data-ttu-id="077bd-138">Új – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="077bd-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="077bd-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="077bd-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
