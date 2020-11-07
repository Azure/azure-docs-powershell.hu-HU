---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 0e83ec5266bc807f64bd231a3a423ad8cc7db190
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843926"
---
# <span data-ttu-id="f1e7b-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="f1e7b-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="f1e7b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e7b-103">Töröl egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="f1e7b-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="f1e7b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1e7b-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e7b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1e7b-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e7b-106">Töröl egy IotHub.</span><span class="sxs-lookup"><span data-stu-id="f1e7b-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="f1e7b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1e7b-107">EXAMPLES</span></span>

### <span data-ttu-id="f1e7b-108">Példa 1 IotHub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1e7b-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="f1e7b-109">A "myiothub" nevű IotHub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f1e7b-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="f1e7b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1e7b-110">PARAMETERS</span></span>

### <span data-ttu-id="f1e7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e7b-111">-DefaultProfile</span></span>
<span data-ttu-id="f1e7b-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f1e7b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1e7b-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1e7b-113">-Name</span></span>
<span data-ttu-id="f1e7b-114">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="f1e7b-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e7b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e7b-115">-ResourceGroupName</span></span>
<span data-ttu-id="f1e7b-116">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f1e7b-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e7b-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1e7b-117">-Confirm</span></span>
<span data-ttu-id="f1e7b-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1e7b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e7b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e7b-119">-WhatIf</span></span>
<span data-ttu-id="f1e7b-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1e7b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1e7b-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1e7b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e7b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e7b-122">CommonParameters</span></span>
<span data-ttu-id="f1e7b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1e7b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e7b-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e7b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e7b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e7b-125">INPUTS</span></span>

### <span data-ttu-id="f1e7b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f1e7b-126">System.String</span></span>

## <span data-ttu-id="f1e7b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1e7b-127">OUTPUTS</span></span>

### <span data-ttu-id="f1e7b-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="f1e7b-128">System.Void</span></span>

## <span data-ttu-id="f1e7b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1e7b-129">NOTES</span></span>

## <span data-ttu-id="f1e7b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1e7b-130">RELATED LINKS</span></span>
