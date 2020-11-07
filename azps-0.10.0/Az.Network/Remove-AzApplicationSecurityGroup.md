---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 1bdad35adef15c15c77753c77533f35cfaf945ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841169"
---
# <span data-ttu-id="ee248-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ee248-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="ee248-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ee248-102">SYNOPSIS</span></span>
<span data-ttu-id="ee248-103">Egy alkalmazás biztonsági csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ee248-103">Removes an application security group.</span></span>

## <span data-ttu-id="ee248-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ee248-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee248-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ee248-105">DESCRIPTION</span></span>
<span data-ttu-id="ee248-106">A **Remove-AzApplicationSecurityGroup** parancsmag eltávolítja az alkalmazások biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="ee248-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="ee248-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ee248-107">EXAMPLES</span></span>

### <span data-ttu-id="ee248-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ee248-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ee248-109">Ez a parancs törli a MyApplicationSecurityGrouo nevű alkalmazás biztonsági csoportját a MyResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="ee248-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ee248-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ee248-110">PARAMETERS</span></span>

### <span data-ttu-id="ee248-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee248-111">-DefaultProfile</span></span>
<span data-ttu-id="ee248-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee248-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee248-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ee248-113">-Force</span></span>
<span data-ttu-id="ee248-114">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="ee248-114">Do not ask for confirmation if you want to delete resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee248-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ee248-115">-Name</span></span>
<span data-ttu-id="ee248-116">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="ee248-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee248-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee248-117">-PassThru</span></span>
<span data-ttu-id="ee248-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="ee248-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ee248-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ee248-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee248-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee248-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee248-121">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee248-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee248-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ee248-122">-Confirm</span></span>
<span data-ttu-id="ee248-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ee248-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee248-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee248-124">-WhatIf</span></span>
<span data-ttu-id="ee248-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ee248-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee248-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ee248-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee248-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee248-127">CommonParameters</span></span>
<span data-ttu-id="ee248-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ee248-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee248-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee248-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee248-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee248-130">INPUTS</span></span>

### <span data-ttu-id="ee248-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ee248-131">System.String</span></span>

## <span data-ttu-id="ee248-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee248-132">OUTPUTS</span></span>

### <span data-ttu-id="ee248-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="ee248-133">System.Object</span></span>

## <span data-ttu-id="ee248-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ee248-134">NOTES</span></span>

## <span data-ttu-id="ee248-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee248-135">RELATED LINKS</span></span>

[<span data-ttu-id="ee248-136">Új – AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ee248-136">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="ee248-137">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ee248-137">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
