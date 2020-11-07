---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 48121e165eea27b57ec36301a657a6778f4c14b7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848733"
---
# <span data-ttu-id="838e9-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="838e9-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="838e9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="838e9-102">SYNOPSIS</span></span>
<span data-ttu-id="838e9-103">Egy alkalmazás biztonsági csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="838e9-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="838e9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="838e9-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="838e9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="838e9-105">DESCRIPTION</span></span>
<span data-ttu-id="838e9-106">A **Remove-AzureRmApplicationSecurityGroup** parancsmag eltávolítja az alkalmazások biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="838e9-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="838e9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="838e9-107">EXAMPLES</span></span>

### <span data-ttu-id="838e9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="838e9-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="838e9-109">Ez a parancs törli a MyApplicationSecurityGrouo nevű alkalmazás biztonsági csoportját a MyResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="838e9-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="838e9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="838e9-110">PARAMETERS</span></span>

### <span data-ttu-id="838e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838e9-111">-DefaultProfile</span></span>
<span data-ttu-id="838e9-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="838e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="838e9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="838e9-113">-Force</span></span>
<span data-ttu-id="838e9-114">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="838e9-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="838e9-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="838e9-115">-Name</span></span>
<span data-ttu-id="838e9-116">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="838e9-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="838e9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="838e9-117">-PassThru</span></span>
<span data-ttu-id="838e9-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="838e9-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="838e9-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="838e9-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="838e9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="838e9-120">-ResourceGroupName</span></span>
<span data-ttu-id="838e9-121">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="838e9-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="838e9-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="838e9-122">-Confirm</span></span>
<span data-ttu-id="838e9-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="838e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="838e9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="838e9-124">-WhatIf</span></span>
<span data-ttu-id="838e9-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="838e9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="838e9-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="838e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="838e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838e9-127">CommonParameters</span></span>
<span data-ttu-id="838e9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="838e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838e9-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838e9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838e9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="838e9-130">INPUTS</span></span>

### <span data-ttu-id="838e9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="838e9-131">System.String</span></span>

## <span data-ttu-id="838e9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="838e9-132">OUTPUTS</span></span>

### <span data-ttu-id="838e9-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="838e9-133">System.Object</span></span>

## <span data-ttu-id="838e9-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="838e9-134">NOTES</span></span>

## <span data-ttu-id="838e9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="838e9-135">RELATED LINKS</span></span>

[<span data-ttu-id="838e9-136">Új – AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="838e9-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="838e9-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="838e9-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)