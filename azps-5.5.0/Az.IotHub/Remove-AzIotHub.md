---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167322"
---
# <span data-ttu-id="7a482-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="7a482-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="7a482-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a482-102">SYNOPSIS</span></span>
<span data-ttu-id="7a482-103">Töröl egy IotHubot.</span><span class="sxs-lookup"><span data-stu-id="7a482-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="7a482-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7a482-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a482-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7a482-105">DESCRIPTION</span></span>
<span data-ttu-id="7a482-106">Töröl egy IotHubot.</span><span class="sxs-lookup"><span data-stu-id="7a482-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="7a482-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7a482-107">EXAMPLES</span></span>

### <span data-ttu-id="7a482-108">1. példa: IotHub eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7a482-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="7a482-109">Eltávolít egy "myiothub" nevű IotHubot.</span><span class="sxs-lookup"><span data-stu-id="7a482-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="7a482-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a482-110">PARAMETERS</span></span>

### <span data-ttu-id="7a482-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a482-111">-DefaultProfile</span></span>
<span data-ttu-id="7a482-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7a482-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a482-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7a482-113">-Name</span></span>
<span data-ttu-id="7a482-114">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="7a482-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="7a482-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a482-115">-ResourceGroupName</span></span>
<span data-ttu-id="7a482-116">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7a482-116">Resource Group Name</span></span>

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

### <span data-ttu-id="7a482-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a482-117">-Confirm</span></span>
<span data-ttu-id="7a482-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7a482-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a482-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a482-119">-WhatIf</span></span>
<span data-ttu-id="7a482-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7a482-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a482-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7a482-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a482-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a482-122">CommonParameters</span></span>
<span data-ttu-id="7a482-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a482-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a482-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a482-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a482-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a482-125">INPUTS</span></span>

### <span data-ttu-id="7a482-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7a482-126">System.String</span></span>

## <span data-ttu-id="7a482-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7a482-127">OUTPUTS</span></span>

### <span data-ttu-id="7a482-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="7a482-128">System.Void</span></span>

## <span data-ttu-id="7a482-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7a482-129">NOTES</span></span>

## <span data-ttu-id="7a482-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7a482-130">RELATED LINKS</span></span>
