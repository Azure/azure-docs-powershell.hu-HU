---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 2e39f313e5f6d9c13a9eeb7f4365901ebbea4c9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494466"
---
# <span data-ttu-id="8d2a4-101">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8d2a4-101">Remove-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="8d2a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2a4-103">Egy alkalmazás biztonsági csoportjának eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-103">Removes an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d2a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d2a4-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d2a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d2a4-105">DESCRIPTION</span></span>
<span data-ttu-id="8d2a4-106">A **Remove-AzureRmApplicationSecurityGroup** parancsmag eltávolítja az alkalmazások biztonsági csoportját.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-106">The **Remove-AzureRmApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="8d2a4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8d2a4-107">EXAMPLES</span></span>

### <span data-ttu-id="8d2a4-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8d2a4-108">Example 1</span></span>
```
PS C:\>Remove-AzureRmApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8d2a4-109">Ez a parancs törli a MyApplicationSecurityGrouo nevű alkalmazás biztonsági csoportját a MyResourceGroup nevű erőforráscsoport nevében.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="8d2a4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d2a4-110">PARAMETERS</span></span>

### <span data-ttu-id="8d2a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2a4-111">-DefaultProfile</span></span>
<span data-ttu-id="8d2a4-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d2a4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8d2a4-113">-Force</span></span>
<span data-ttu-id="8d2a4-114">Nem kér megerősítést, ha az erőforrást törölni szeretné</span><span class="sxs-lookup"><span data-stu-id="8d2a4-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8d2a4-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d2a4-115">-Name</span></span>
<span data-ttu-id="8d2a4-116">Az alkalmazás biztonsági csoportjának neve.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-116">The name of the application security group.</span></span>

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

### <span data-ttu-id="8d2a4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d2a4-117">-PassThru</span></span>
<span data-ttu-id="8d2a4-118">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8d2a4-119">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8d2a4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2a4-120">-ResourceGroupName</span></span>
<span data-ttu-id="8d2a4-121">Az alkalmazás biztonsági csoportjának erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-121">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="8d2a4-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8d2a4-122">-Confirm</span></span>
<span data-ttu-id="8d2a4-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d2a4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d2a4-124">-WhatIf</span></span>
<span data-ttu-id="8d2a4-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d2a4-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8d2a4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d2a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2a4-127">CommonParameters</span></span>
<span data-ttu-id="8d2a4-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d2a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2a4-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d2a4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2a4-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d2a4-130">INPUTS</span></span>

### <span data-ttu-id="8d2a4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8d2a4-131">System.String</span></span>

## <span data-ttu-id="8d2a4-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d2a4-132">OUTPUTS</span></span>

### <span data-ttu-id="8d2a4-133">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="8d2a4-133">System.Object</span></span>

## <span data-ttu-id="8d2a4-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d2a4-134">NOTES</span></span>

## <span data-ttu-id="8d2a4-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d2a4-135">RELATED LINKS</span></span>

[<span data-ttu-id="8d2a4-136">Új – AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8d2a4-136">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="8d2a4-137">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8d2a4-137">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)
