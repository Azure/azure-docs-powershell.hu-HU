---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 78478b28e42302ad3a672a0ee889f03807f3d1ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935753"
---
# <span data-ttu-id="3f63e-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="3f63e-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="3f63e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f63e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f63e-103">Töröl egy IotHubot.</span><span class="sxs-lookup"><span data-stu-id="3f63e-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="3f63e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f63e-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f63e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f63e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f63e-106">Töröl egy IotHubot.</span><span class="sxs-lookup"><span data-stu-id="3f63e-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="3f63e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f63e-107">EXAMPLES</span></span>

### <span data-ttu-id="3f63e-108">1. példa: IotHub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3f63e-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="3f63e-109">Eltávolít egy "myiothub" nevű IotHubot.</span><span class="sxs-lookup"><span data-stu-id="3f63e-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="3f63e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f63e-110">PARAMETERS</span></span>

### <span data-ttu-id="3f63e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f63e-111">-DefaultProfile</span></span>
<span data-ttu-id="3f63e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3f63e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f63e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3f63e-113">-Name</span></span>
<span data-ttu-id="3f63e-114">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="3f63e-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="3f63e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f63e-115">-ResourceGroupName</span></span>
<span data-ttu-id="3f63e-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3f63e-116">Resource Group Name</span></span>

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

### <span data-ttu-id="3f63e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f63e-117">-Confirm</span></span>
<span data-ttu-id="3f63e-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3f63e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f63e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f63e-119">-WhatIf</span></span>
<span data-ttu-id="3f63e-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3f63e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f63e-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f63e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f63e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f63e-122">CommonParameters</span></span>
<span data-ttu-id="3f63e-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f63e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f63e-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f63e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f63e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f63e-125">INPUTS</span></span>

### <span data-ttu-id="3f63e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="3f63e-126">System.String</span></span>

## <span data-ttu-id="3f63e-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f63e-127">OUTPUTS</span></span>

### <span data-ttu-id="3f63e-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="3f63e-128">System.Void</span></span>

## <span data-ttu-id="3f63e-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f63e-129">NOTES</span></span>

## <span data-ttu-id="3f63e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f63e-130">RELATED LINKS</span></span>
