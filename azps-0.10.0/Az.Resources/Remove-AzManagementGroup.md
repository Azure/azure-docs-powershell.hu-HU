---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: 9ac7717769cef1ad147ea122ddedde3efd1e389f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843257"
---
# <span data-ttu-id="36d98-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="36d98-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="36d98-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36d98-102">SYNOPSIS</span></span>
<span data-ttu-id="36d98-103">Felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36d98-103">Removes a Management Group</span></span>

## <span data-ttu-id="36d98-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36d98-104">SYNTAX</span></span>

### <span data-ttu-id="36d98-105">GroupOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="36d98-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36d98-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="36d98-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d98-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="36d98-107">DESCRIPTION</span></span>
<span data-ttu-id="36d98-108">A **Remove-AzManagementGroup** parancsmag egy felügyeleti csoportot töröl.</span><span class="sxs-lookup"><span data-stu-id="36d98-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="36d98-109">Példák</span><span class="sxs-lookup"><span data-stu-id="36d98-109">EXAMPLES</span></span>

### <span data-ttu-id="36d98-110">Példa 1 – felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="36d98-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="36d98-111">2. példa – egy felügyeleti csoport eltávolítása a csőhálózat-PSManagementGroup objektumból</span><span class="sxs-lookup"><span data-stu-id="36d98-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="36d98-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36d98-112">PARAMETERS</span></span>

### <span data-ttu-id="36d98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d98-113">-DefaultProfile</span></span>
<span data-ttu-id="36d98-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="36d98-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d98-115">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="36d98-115">-GroupName</span></span>
<span data-ttu-id="36d98-116">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="36d98-116">Management Group Id</span></span>

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

### <span data-ttu-id="36d98-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36d98-117">-InputObject</span></span>
<span data-ttu-id="36d98-118">Beviteli objektum a hívás kérése</span><span class="sxs-lookup"><span data-stu-id="36d98-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="36d98-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36d98-119">-PassThru</span></span>
<span data-ttu-id="36d98-120">Sikeres végrehajtás visszaadása `true`</span><span class="sxs-lookup"><span data-stu-id="36d98-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="36d98-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="36d98-121">-Confirm</span></span>
<span data-ttu-id="36d98-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="36d98-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d98-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d98-123">-WhatIf</span></span>
<span data-ttu-id="36d98-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="36d98-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d98-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="36d98-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d98-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d98-126">CommonParameters</span></span>
<span data-ttu-id="36d98-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36d98-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d98-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d98-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d98-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d98-129">INPUTS</span></span>

### <span data-ttu-id="36d98-130">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="36d98-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="36d98-131">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36d98-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="36d98-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36d98-132">OUTPUTS</span></span>

### <span data-ttu-id="36d98-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36d98-133">System.Boolean</span></span>

## <span data-ttu-id="36d98-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36d98-134">NOTES</span></span>

## <span data-ttu-id="36d98-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36d98-135">RELATED LINKS</span></span>
