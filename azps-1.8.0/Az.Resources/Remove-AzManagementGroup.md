---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: cbc6be671669b3db8af41c0e5de4333b811e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669344"
---
# <span data-ttu-id="3e842-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e842-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="3e842-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3e842-102">SYNOPSIS</span></span>
<span data-ttu-id="3e842-103">Felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3e842-103">Removes a Management Group</span></span>

## <span data-ttu-id="3e842-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3e842-104">SYNTAX</span></span>

### <span data-ttu-id="3e842-105">GroupOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3e842-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e842-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="3e842-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e842-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3e842-107">DESCRIPTION</span></span>
<span data-ttu-id="3e842-108">A **Remove-AzManagementGroup** parancsmag egy felügyeleti csoportot töröl.</span><span class="sxs-lookup"><span data-stu-id="3e842-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="3e842-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3e842-109">EXAMPLES</span></span>

### <span data-ttu-id="3e842-110">Példa 1 – felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="3e842-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="3e842-111">2. példa – egy felügyeleti csoport eltávolítása a csőhálózat-PSManagementGroup objektumból</span><span class="sxs-lookup"><span data-stu-id="3e842-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="3e842-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3e842-112">PARAMETERS</span></span>

### <span data-ttu-id="3e842-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e842-113">-DefaultProfile</span></span>
<span data-ttu-id="3e842-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3e842-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e842-115">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="3e842-115">-GroupName</span></span>
<span data-ttu-id="3e842-116">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="3e842-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e842-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e842-117">-InputObject</span></span>
<span data-ttu-id="3e842-118">Beviteli objektum a hívás kérése</span><span class="sxs-lookup"><span data-stu-id="3e842-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e842-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e842-119">-PassThru</span></span>
<span data-ttu-id="3e842-120">Sikeres végrehajtás visszaadása `true`</span><span class="sxs-lookup"><span data-stu-id="3e842-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="3e842-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3e842-121">-Confirm</span></span>
<span data-ttu-id="3e842-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3e842-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e842-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e842-123">-WhatIf</span></span>
<span data-ttu-id="3e842-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3e842-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e842-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3e842-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e842-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e842-126">CommonParameters</span></span>
<span data-ttu-id="3e842-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3e842-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e842-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e842-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e842-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e842-129">INPUTS</span></span>

### <span data-ttu-id="3e842-130">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="3e842-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="3e842-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3e842-131">OUTPUTS</span></span>

### <span data-ttu-id="3e842-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e842-132">System.Boolean</span></span>

## <span data-ttu-id="3e842-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3e842-133">NOTES</span></span>

## <span data-ttu-id="3e842-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3e842-134">RELATED LINKS</span></span>
