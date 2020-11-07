---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0af35c08cce181ba96f15ca77c0f17f96cfeb32e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670190"
---
# <span data-ttu-id="12694-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="12694-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="12694-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="12694-102">SYNOPSIS</span></span>
<span data-ttu-id="12694-103">Egy alkalmazás biztonsági csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="12694-103">Removes an application security group.</span></span>

## <span data-ttu-id="12694-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="12694-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12694-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="12694-105">DESCRIPTION</span></span>
<span data-ttu-id="12694-106">A **Remove-AzApplicationSecurityGroup** parancsmag eltávolítja az alkalmazások biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="12694-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="12694-107">Példák</span><span class="sxs-lookup"><span data-stu-id="12694-107">EXAMPLES</span></span>

### <span data-ttu-id="12694-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="12694-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="12694-109">Ez a parancs törli a MyApplicationSecurityGrouo nevű alkalmazás biztonsági csoportját a MyResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="12694-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="12694-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="12694-110">PARAMETERS</span></span>

### <span data-ttu-id="12694-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12694-111">-AsJob</span></span>
<span data-ttu-id="12694-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="12694-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12694-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12694-113">-DefaultProfile</span></span>
<span data-ttu-id="12694-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="12694-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12694-115">-Force</span><span class="sxs-lookup"><span data-stu-id="12694-115">-Force</span></span>
<span data-ttu-id="12694-116">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="12694-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="12694-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="12694-117">-Name</span></span>
<span data-ttu-id="12694-118">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="12694-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="12694-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12694-119">-PassThru</span></span>
<span data-ttu-id="12694-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="12694-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="12694-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="12694-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12694-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12694-122">-ResourceGroupName</span></span>
<span data-ttu-id="12694-123">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="12694-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="12694-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="12694-124">-Confirm</span></span>
<span data-ttu-id="12694-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="12694-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12694-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12694-126">-WhatIf</span></span>
<span data-ttu-id="12694-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="12694-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12694-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="12694-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12694-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12694-129">CommonParameters</span></span>
<span data-ttu-id="12694-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="12694-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12694-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12694-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12694-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="12694-132">INPUTS</span></span>

### <span data-ttu-id="12694-133">System. String</span><span class="sxs-lookup"><span data-stu-id="12694-133">System.String</span></span>

## <span data-ttu-id="12694-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="12694-134">OUTPUTS</span></span>

### <span data-ttu-id="12694-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12694-135">System.Boolean</span></span>

## <span data-ttu-id="12694-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="12694-136">NOTES</span></span>

## <span data-ttu-id="12694-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="12694-137">RELATED LINKS</span></span>

[<span data-ttu-id="12694-138">Új – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="12694-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="12694-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="12694-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
