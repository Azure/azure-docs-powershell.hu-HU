---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 1da7b9981b3c2fe96d895290b7ab73dfc36e183e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496516"
---
# <span data-ttu-id="2f527-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="2f527-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="2f527-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2f527-102">SYNOPSIS</span></span>
<span data-ttu-id="2f527-103">Töröl egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="2f527-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f527-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2f527-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f527-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2f527-105">DESCRIPTION</span></span>
<span data-ttu-id="2f527-106">Töröl egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="2f527-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="2f527-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2f527-107">EXAMPLES</span></span>

### <span data-ttu-id="2f527-108">Példa 1 IotHub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2f527-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2f527-109">A "myiothub" nevű IotHub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2f527-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="2f527-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2f527-110">PARAMETERS</span></span>

### <span data-ttu-id="2f527-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f527-111">-DefaultProfile</span></span>
<span data-ttu-id="2f527-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2f527-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f527-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2f527-113">-Name</span></span>
<span data-ttu-id="2f527-114">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="2f527-114">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f527-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f527-115">-ResourceGroupName</span></span>
<span data-ttu-id="2f527-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="2f527-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f527-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2f527-117">-Confirm</span></span>
<span data-ttu-id="2f527-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2f527-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f527-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f527-119">-WhatIf</span></span>
<span data-ttu-id="2f527-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2f527-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f527-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2f527-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f527-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f527-122">CommonParameters</span></span>
<span data-ttu-id="2f527-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2f527-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f527-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f527-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f527-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f527-125">INPUTS</span></span>

### <span data-ttu-id="2f527-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2f527-126">System.String</span></span>

## <span data-ttu-id="2f527-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2f527-127">OUTPUTS</span></span>

### <span data-ttu-id="2f527-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="2f527-128">System.Object</span></span>

## <span data-ttu-id="2f527-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2f527-129">NOTES</span></span>

## <span data-ttu-id="2f527-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2f527-130">RELATED LINKS</span></span>

