---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353297"
---
# <span data-ttu-id="bee01-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="bee01-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="bee01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee01-102">SYNOPSIS</span></span>
<span data-ttu-id="bee01-103">Egy atteesztálás törlése.</span><span class="sxs-lookup"><span data-stu-id="bee01-103">Deletes an attestation.</span></span>

## <span data-ttu-id="bee01-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bee01-104">SYNTAX</span></span>

### <span data-ttu-id="bee01-105">ByAvailableAttestation (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bee01-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bee01-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="bee01-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bee01-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="bee01-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bee01-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bee01-108">DESCRIPTION</span></span>
<span data-ttu-id="bee01-109">A Remove-AzAttestation parancsmag törli a megadott igazolást.</span><span class="sxs-lookup"><span data-stu-id="bee01-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="bee01-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bee01-110">EXAMPLES</span></span>

### <span data-ttu-id="bee01-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="bee01-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="bee01-112">Törölje a psh-test-rg nevű *erőforráscsoport pshtest3* nevű szolgáltatóját az aktuális előfizetésből. </span><span class="sxs-lookup"><span data-stu-id="bee01-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="bee01-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bee01-113">PARAMETERS</span></span>

### <span data-ttu-id="bee01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee01-114">-DefaultProfile</span></span>
<span data-ttu-id="bee01-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bee01-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bee01-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bee01-116">-InputObject</span></span>
<span data-ttu-id="bee01-117">Attestation object to bedeleted.</span><span class="sxs-lookup"><span data-stu-id="bee01-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="bee01-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bee01-118">-Name</span></span>
<span data-ttu-id="bee01-119">Az eltávolítható igazolás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bee01-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="bee01-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bee01-120">-PassThru</span></span>
<span data-ttu-id="bee01-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="bee01-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bee01-122">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="bee01-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bee01-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee01-123">-ResourceGroupName</span></span>
<span data-ttu-id="bee01-124">Az eltávolítható Azure-attestation erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bee01-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="bee01-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bee01-125">-ResourceId</span></span>
<span data-ttu-id="bee01-126">Attestation Resource Id.</span><span class="sxs-lookup"><span data-stu-id="bee01-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="bee01-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bee01-127">-Confirm</span></span>
<span data-ttu-id="bee01-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bee01-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bee01-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee01-129">-WhatIf</span></span>
<span data-ttu-id="bee01-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bee01-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee01-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bee01-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bee01-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee01-132">CommonParameters</span></span>
<span data-ttu-id="bee01-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee01-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee01-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bee01-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee01-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bee01-135">INPUTS</span></span>

### <span data-ttu-id="bee01-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bee01-136">System.String</span></span>

### <span data-ttu-id="bee01-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="bee01-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="bee01-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bee01-138">OUTPUTS</span></span>

### <span data-ttu-id="bee01-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bee01-139">System.Boolean</span></span>

## <span data-ttu-id="bee01-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bee01-140">NOTES</span></span>

## <span data-ttu-id="bee01-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bee01-141">RELATED LINKS</span></span>
