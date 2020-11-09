---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300554"
---
# <span data-ttu-id="ba8dc-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ba8dc-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="ba8dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8dc-103">Felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ba8dc-103">Removes a Management Group</span></span>

## <span data-ttu-id="ba8dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba8dc-104">SYNTAX</span></span>

### <span data-ttu-id="ba8dc-105">GroupOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba8dc-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba8dc-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="ba8dc-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba8dc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba8dc-107">DESCRIPTION</span></span>
<span data-ttu-id="ba8dc-108">A **Remove-AzManagementGroup** parancsmag egy felügyeleti csoportot töröl.</span><span class="sxs-lookup"><span data-stu-id="ba8dc-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="ba8dc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ba8dc-109">EXAMPLES</span></span>

### <span data-ttu-id="ba8dc-110">Példa 1: felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="ba8dc-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="ba8dc-111">2. példa: felügyeleti csoport eltávolítása a csővezetékek PSManagementGroup objektumból</span><span class="sxs-lookup"><span data-stu-id="ba8dc-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="ba8dc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba8dc-112">PARAMETERS</span></span>

### <span data-ttu-id="ba8dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8dc-113">-DefaultProfile</span></span>
<span data-ttu-id="ba8dc-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ba8dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba8dc-115">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="ba8dc-115">-GroupName</span></span>
<span data-ttu-id="ba8dc-116">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="ba8dc-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8dc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba8dc-117">-InputObject</span></span>
<span data-ttu-id="ba8dc-118">Beviteli objektum a hívás kérése</span><span class="sxs-lookup"><span data-stu-id="ba8dc-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="ba8dc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba8dc-119">-PassThru</span></span>
<span data-ttu-id="ba8dc-120">Sikeres végrehajtás visszaadása `true`</span><span class="sxs-lookup"><span data-stu-id="ba8dc-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="ba8dc-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba8dc-121">-Confirm</span></span>
<span data-ttu-id="ba8dc-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba8dc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8dc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba8dc-123">-WhatIf</span></span>
<span data-ttu-id="ba8dc-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba8dc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba8dc-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba8dc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba8dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8dc-126">CommonParameters</span></span>
<span data-ttu-id="ba8dc-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba8dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8dc-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ba8dc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8dc-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba8dc-129">INPUTS</span></span>

### <span data-ttu-id="ba8dc-130">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ba8dc-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="ba8dc-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba8dc-131">OUTPUTS</span></span>

### <span data-ttu-id="ba8dc-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ba8dc-132">System.Boolean</span></span>

## <span data-ttu-id="ba8dc-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba8dc-133">NOTES</span></span>

## <span data-ttu-id="ba8dc-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba8dc-134">RELATED LINKS</span></span>
