---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185961"
---
# <span data-ttu-id="ae859-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ae859-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="ae859-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae859-102">SYNOPSIS</span></span>
<span data-ttu-id="ae859-103">Egy alkalmazás biztonsági csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ae859-103">Removes an application security group.</span></span>

## <span data-ttu-id="ae859-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae859-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae859-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae859-105">DESCRIPTION</span></span>
<span data-ttu-id="ae859-106">A **Remove-AzApplicationSecurityGroup** parancsmag eltávolítja az alkalmazások biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="ae859-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="ae859-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ae859-107">EXAMPLES</span></span>

### <span data-ttu-id="ae859-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ae859-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ae859-109">Ez a parancs törli a MyApplicationSecurityGrouo nevű alkalmazás biztonsági csoportját a MyResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="ae859-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ae859-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae859-110">PARAMETERS</span></span>

### <span data-ttu-id="ae859-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae859-111">-AsJob</span></span>
<span data-ttu-id="ae859-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="ae859-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae859-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae859-113">-DefaultProfile</span></span>
<span data-ttu-id="ae859-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae859-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae859-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ae859-115">-Force</span></span>
<span data-ttu-id="ae859-116">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="ae859-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ae859-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae859-117">-Name</span></span>
<span data-ttu-id="ae859-118">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="ae859-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="ae859-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae859-119">-PassThru</span></span>
<span data-ttu-id="ae859-120">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ae859-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ae859-121">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ae859-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae859-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae859-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae859-123">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ae859-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="ae859-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ae859-124">-Confirm</span></span>
<span data-ttu-id="ae859-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ae859-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae859-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae859-126">-WhatIf</span></span>
<span data-ttu-id="ae859-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ae859-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae859-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ae859-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae859-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae859-129">CommonParameters</span></span>
<span data-ttu-id="ae859-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae859-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae859-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae859-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae859-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae859-132">INPUTS</span></span>

### <span data-ttu-id="ae859-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ae859-133">System.String</span></span>

## <span data-ttu-id="ae859-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae859-134">OUTPUTS</span></span>

### <span data-ttu-id="ae859-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae859-135">System.Boolean</span></span>

## <span data-ttu-id="ae859-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae859-136">NOTES</span></span>

## <span data-ttu-id="ae859-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae859-137">RELATED LINKS</span></span>

[<span data-ttu-id="ae859-138">Új – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ae859-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="ae859-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ae859-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
