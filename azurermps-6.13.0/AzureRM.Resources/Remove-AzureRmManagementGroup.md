---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagementGroup.md
ms.openlocfilehash: 7f19e45f96dbeac1470fbcc67a7db319589ad390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501975"
---
# <span data-ttu-id="f6b06-101">Remove-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f6b06-101">Remove-AzureRmManagementGroup</span></span>

## <span data-ttu-id="f6b06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6b06-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b06-103">Felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f6b06-103">Removes a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6b06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6b06-104">SYNTAX</span></span>

### <span data-ttu-id="f6b06-105">GroupOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f6b06-105">GroupOperations (Default)</span></span>
```
Remove-AzureRmManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6b06-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="f6b06-106">ManagementGroupObject</span></span>
```
Remove-AzureRmManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6b06-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6b06-107">DESCRIPTION</span></span>
<span data-ttu-id="f6b06-108">A **Remove-AzureRmManagementGroup** parancsmag egy felügyeleti csoportot töröl.</span><span class="sxs-lookup"><span data-stu-id="f6b06-108">The **Remove-AzureRmManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="f6b06-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f6b06-109">EXAMPLES</span></span>

### <span data-ttu-id="f6b06-110">Példa 1 – felügyeleti csoport eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f6b06-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzureRmManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="f6b06-111">2. példa – egy felügyeleti csoport eltávolítása a csőhálózat-PSManagementGroup objektumból</span><span class="sxs-lookup"><span data-stu-id="f6b06-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzureRmManagementGroup -GroupName "TestGroup" | Remove-AzureRmManagementGroup
```

## <span data-ttu-id="f6b06-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6b06-112">PARAMETERS</span></span>

### <span data-ttu-id="f6b06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b06-113">-DefaultProfile</span></span>
<span data-ttu-id="f6b06-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6b06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b06-115">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="f6b06-115">-GroupName</span></span>
<span data-ttu-id="f6b06-116">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="f6b06-116">Management Group Id</span></span>

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

### <span data-ttu-id="f6b06-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6b06-117">-InputObject</span></span>
<span data-ttu-id="f6b06-118">Beviteli objektum a hívás kérése</span><span class="sxs-lookup"><span data-stu-id="f6b06-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="f6b06-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6b06-119">-PassThru</span></span>
<span data-ttu-id="f6b06-120">Sikeres végrehajtás visszaadása `true`</span><span class="sxs-lookup"><span data-stu-id="f6b06-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="f6b06-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6b06-121">-Confirm</span></span>
<span data-ttu-id="f6b06-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6b06-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6b06-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6b06-123">-WhatIf</span></span>
<span data-ttu-id="f6b06-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6b06-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6b06-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6b06-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6b06-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b06-126">CommonParameters</span></span>
<span data-ttu-id="f6b06-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6b06-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b06-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b06-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b06-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6b06-129">INPUTS</span></span>

### <span data-ttu-id="f6b06-130">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f6b06-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="f6b06-131">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f6b06-131">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f6b06-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6b06-132">OUTPUTS</span></span>

### <span data-ttu-id="f6b06-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6b06-133">System.Boolean</span></span>

## <span data-ttu-id="f6b06-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6b06-134">NOTES</span></span>

## <span data-ttu-id="f6b06-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6b06-135">RELATED LINKS</span></span>
