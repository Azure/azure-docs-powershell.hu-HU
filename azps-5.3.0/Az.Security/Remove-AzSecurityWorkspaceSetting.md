---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479761"
---
# <span data-ttu-id="824eb-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="824eb-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="824eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824eb-102">SYNOPSIS</span></span>
<span data-ttu-id="824eb-103">Törli az előfizetés biztonsági munkaterületének beállítását.</span><span class="sxs-lookup"><span data-stu-id="824eb-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="824eb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="824eb-104">SYNTAX</span></span>

### <span data-ttu-id="824eb-105">SubscriptionLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="824eb-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824eb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="824eb-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824eb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="824eb-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824eb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="824eb-108">DESCRIPTION</span></span>
<span data-ttu-id="824eb-109">Törli az előfizetés biztonsági munkaterületének beállítását.</span><span class="sxs-lookup"><span data-stu-id="824eb-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="824eb-110">Ez a művelet lehetővé teszi az újonnan telepített biztonsági ügynököknek, hogy az előfizetés alapértelmezett munkaterületére jelentsen.</span><span class="sxs-lookup"><span data-stu-id="824eb-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="824eb-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="824eb-111">EXAMPLES</span></span>

### <span data-ttu-id="824eb-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="824eb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="824eb-113">Törli az előfizetés biztonsági munkaterületének beállítását.</span><span class="sxs-lookup"><span data-stu-id="824eb-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="824eb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="824eb-114">PARAMETERS</span></span>

### <span data-ttu-id="824eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824eb-115">-DefaultProfile</span></span>
<span data-ttu-id="824eb-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="824eb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="824eb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="824eb-117">-InputObject</span></span>
<span data-ttu-id="824eb-118">Bemeneti objektum.</span><span class="sxs-lookup"><span data-stu-id="824eb-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="824eb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="824eb-119">-Name</span></span>
<span data-ttu-id="824eb-120">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="824eb-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824eb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="824eb-121">-PassThru</span></span>
<span data-ttu-id="824eb-122">Adja vissza, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="824eb-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="824eb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="824eb-123">-ResourceId</span></span>
<span data-ttu-id="824eb-124">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="824eb-124">Resource ID.</span></span>

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

### <span data-ttu-id="824eb-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="824eb-125">-Confirm</span></span>
<span data-ttu-id="824eb-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="824eb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824eb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824eb-127">-WhatIf</span></span>
<span data-ttu-id="824eb-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="824eb-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="824eb-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="824eb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824eb-130">CommonParameters</span></span>
<span data-ttu-id="824eb-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824eb-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="824eb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824eb-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="824eb-133">INPUTS</span></span>

### <span data-ttu-id="824eb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="824eb-134">System.String</span></span>

### <span data-ttu-id="824eb-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="824eb-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="824eb-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="824eb-136">OUTPUTS</span></span>

### <span data-ttu-id="824eb-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="824eb-137">System.Boolean</span></span>

## <span data-ttu-id="824eb-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="824eb-138">NOTES</span></span>

## <span data-ttu-id="824eb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="824eb-139">RELATED LINKS</span></span>
