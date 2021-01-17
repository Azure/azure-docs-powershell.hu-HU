---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353286"
---
# <span data-ttu-id="bdb86-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="bdb86-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="bdb86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb86-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb86-103">Alaphelyzetbe állítja a házirendet egy bérlői fiókból az Azure Attestationnben.}</span><span class="sxs-lookup"><span data-stu-id="bdb86-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="bdb86-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bdb86-104">SYNTAX</span></span>

### <span data-ttu-id="bdb86-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb86-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb86-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdb86-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb86-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bdb86-107">DESCRIPTION</span></span>
<span data-ttu-id="bdb86-108">A Reset-AzAttestationPolicy parancsmag alaphelyzetbe állítja a felhasználó által definiált előfizetési házirendet egy bérlői fiókból az Azure Attestation szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="bdb86-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="bdb86-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bdb86-109">EXAMPLES</span></span>

### <span data-ttu-id="bdb86-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="bdb86-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="bdb86-111">Állítsa vissza a házirendet az alapértelmezettre az Attestation Provider *pshtest* for Tee type *SgxEnclave* esetén.</span><span class="sxs-lookup"><span data-stu-id="bdb86-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="bdb86-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="bdb86-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="bdb86-113">Ha az Attestation Provider *pshtest* az különálló megbízhatósági modell használatára van konfigurálva, állítsa vissza a házirendet az alapértelmezettre a Tee típusú *SgxEnclave* esetén egy aláírt házirendet megjelölve.</span><span class="sxs-lookup"><span data-stu-id="bdb86-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="bdb86-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdb86-114">PARAMETERS</span></span>

### <span data-ttu-id="bdb86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb86-115">-DefaultProfile</span></span>
<span data-ttu-id="bdb86-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bdb86-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb86-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bdb86-117">-Name</span></span>
<span data-ttu-id="bdb86-118">Megadja a bérlő nevét.</span><span class="sxs-lookup"><span data-stu-id="bdb86-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="bdb86-119">Ez a parancsmag alaphelyzetbe állítja a paraméter által megadott bérlői házirendet.</span><span class="sxs-lookup"><span data-stu-id="bdb86-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb86-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdb86-120">-PassThru</span></span>
<span data-ttu-id="bdb86-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="bdb86-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bdb86-122">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="bdb86-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bdb86-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="bdb86-123">-Policy</span></span>
<span data-ttu-id="bdb86-124">A visszaállítható házirenddokumentumot leíró JSON webtoken.</span><span class="sxs-lookup"><span data-stu-id="bdb86-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb86-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb86-125">-ResourceGroupName</span></span>
<span data-ttu-id="bdb86-126">Egy szolgáltató erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdb86-126">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb86-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdb86-127">-ResourceId</span></span>
<span data-ttu-id="bdb86-128">Egy szolgáltató Erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdb86-128">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb86-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="bdb86-129">-Tee</span></span>
<span data-ttu-id="bdb86-130">A megbízható végrehajtási környezet típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="bdb86-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="bdb86-131">Négyféle környezettípust támogatunk: SgxEnclave, OpenEnclave, CyResComponent és VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="bdb86-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb86-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdb86-132">-Confirm</span></span>
<span data-ttu-id="bdb86-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bdb86-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb86-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb86-134">-WhatIf</span></span>
<span data-ttu-id="bdb86-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bdb86-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb86-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bdb86-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb86-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb86-137">CommonParameters</span></span>
<span data-ttu-id="bdb86-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb86-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb86-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdb86-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb86-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bdb86-140">INPUTS</span></span>

### <span data-ttu-id="bdb86-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bdb86-141">System.String</span></span>

## <span data-ttu-id="bdb86-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdb86-142">OUTPUTS</span></span>

### <span data-ttu-id="bdb86-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bdb86-143">System.Boolean</span></span>

## <span data-ttu-id="bdb86-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bdb86-144">NOTES</span></span>

## <span data-ttu-id="bdb86-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdb86-145">RELATED LINKS</span></span>
