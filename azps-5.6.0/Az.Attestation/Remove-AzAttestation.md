---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 564c3d9a67e3a006a7ce7871419e236a71838a42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925225"
---
# <span data-ttu-id="7173e-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="7173e-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="7173e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7173e-102">SYNOPSIS</span></span>
<span data-ttu-id="7173e-103">Egy atteesztálás törlése.</span><span class="sxs-lookup"><span data-stu-id="7173e-103">Deletes an attestation.</span></span>

## <span data-ttu-id="7173e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7173e-104">SYNTAX</span></span>

### <span data-ttu-id="7173e-105">ByAvailableAttestation (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7173e-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7173e-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="7173e-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7173e-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="7173e-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7173e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7173e-108">DESCRIPTION</span></span>
<span data-ttu-id="7173e-109">A Remove-AzAttestation parancsmag törli a megadott igazolást.</span><span class="sxs-lookup"><span data-stu-id="7173e-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="7173e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7173e-110">EXAMPLES</span></span>

### <span data-ttu-id="7173e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7173e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="7173e-112">Törölje a psh-test-rg nevű *erőforráscsoport pshtest3* nevű szolgáltatóját az aktuális előfizetésből. </span><span class="sxs-lookup"><span data-stu-id="7173e-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="7173e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7173e-113">PARAMETERS</span></span>

### <span data-ttu-id="7173e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7173e-114">-DefaultProfile</span></span>
<span data-ttu-id="7173e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7173e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7173e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7173e-116">-InputObject</span></span>
<span data-ttu-id="7173e-117">Attestation object to bedeleted.</span><span class="sxs-lookup"><span data-stu-id="7173e-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7173e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7173e-118">-Name</span></span>
<span data-ttu-id="7173e-119">Az eltávolítható igazolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7173e-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7173e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7173e-120">-PassThru</span></span>
<span data-ttu-id="7173e-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="7173e-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7173e-122">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="7173e-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7173e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7173e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7173e-124">Az eltávolítható Azure-attestation erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7173e-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7173e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7173e-125">-ResourceId</span></span>
<span data-ttu-id="7173e-126">Attestation Resource Id.</span><span class="sxs-lookup"><span data-stu-id="7173e-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7173e-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7173e-127">-Confirm</span></span>
<span data-ttu-id="7173e-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7173e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7173e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7173e-129">-WhatIf</span></span>
<span data-ttu-id="7173e-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7173e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7173e-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7173e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7173e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7173e-132">CommonParameters</span></span>
<span data-ttu-id="7173e-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7173e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7173e-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7173e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7173e-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7173e-135">INPUTS</span></span>

### <span data-ttu-id="7173e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7173e-136">System.String</span></span>

### <span data-ttu-id="7173e-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="7173e-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="7173e-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7173e-138">OUTPUTS</span></span>

### <span data-ttu-id="7173e-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7173e-139">System.Boolean</span></span>

## <span data-ttu-id="7173e-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7173e-140">NOTES</span></span>

## <span data-ttu-id="7173e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7173e-141">RELATED LINKS</span></span>
