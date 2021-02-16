---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 423d79a1dddc95fb6d9437cbfc14d6157ccf8d90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208287"
---
# <span data-ttu-id="175ef-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="175ef-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="175ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="175ef-102">SYNOPSIS</span></span>
<span data-ttu-id="175ef-103">Egy JIT-hálózati hozzáférési házirend törlése.</span><span class="sxs-lookup"><span data-stu-id="175ef-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="175ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="175ef-104">SYNTAX</span></span>

### <span data-ttu-id="175ef-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="175ef-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175ef-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="175ef-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175ef-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="175ef-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="175ef-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="175ef-108">DESCRIPTION</span></span>
<span data-ttu-id="175ef-109">Törli a "Csak az időben" hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="175ef-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="175ef-110">A művelet után a felhasználó nem fog tudni ideiglenes hálózati kapcsolatot kérni a törölt házirendben konfigurált virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="175ef-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="175ef-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="175ef-111">EXAMPLES</span></span>

### <span data-ttu-id="175ef-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="175ef-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="175ef-113">Törli a "Csak az időben" hálózati hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="175ef-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="175ef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="175ef-114">PARAMETERS</span></span>

### <span data-ttu-id="175ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="175ef-115">-DefaultProfile</span></span>
<span data-ttu-id="175ef-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="175ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="175ef-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="175ef-117">-InputObject</span></span>
<span data-ttu-id="175ef-118">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="175ef-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="175ef-119">-Location</span><span class="sxs-lookup"><span data-stu-id="175ef-119">-Location</span></span>
<span data-ttu-id="175ef-120">Hely.</span><span class="sxs-lookup"><span data-stu-id="175ef-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175ef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="175ef-121">-Name</span></span>
<span data-ttu-id="175ef-122">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="175ef-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175ef-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="175ef-123">-PassThru</span></span>
<span data-ttu-id="175ef-124">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="175ef-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="175ef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="175ef-125">-ResourceGroupName</span></span>
<span data-ttu-id="175ef-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="175ef-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175ef-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="175ef-127">-ResourceId</span></span>
<span data-ttu-id="175ef-128">A jit Network Access Policy erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="175ef-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="175ef-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="175ef-129">-Confirm</span></span>
<span data-ttu-id="175ef-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="175ef-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="175ef-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="175ef-131">-WhatIf</span></span>
<span data-ttu-id="175ef-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="175ef-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="175ef-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="175ef-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="175ef-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="175ef-134">CommonParameters</span></span>
<span data-ttu-id="175ef-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="175ef-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="175ef-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="175ef-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="175ef-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="175ef-137">INPUTS</span></span>

### <span data-ttu-id="175ef-138">System.String</span><span class="sxs-lookup"><span data-stu-id="175ef-138">System.String</span></span>

### <span data-ttu-id="175ef-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="175ef-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="175ef-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="175ef-140">OUTPUTS</span></span>

### <span data-ttu-id="175ef-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="175ef-141">System.Boolean</span></span>

## <span data-ttu-id="175ef-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="175ef-142">NOTES</span></span>

## <span data-ttu-id="175ef-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="175ef-143">RELATED LINKS</span></span>
