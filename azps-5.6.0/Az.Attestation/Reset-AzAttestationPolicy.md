---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: b628d93d44b863b4af05f09dd4d132ec986702e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926010"
---
# <span data-ttu-id="08058-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="08058-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="08058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08058-102">SYNOPSIS</span></span>
<span data-ttu-id="08058-103">Alaphelyzetbe állítja a házirendet egy bérlői fiókból az Azure Attestationnben.}</span><span class="sxs-lookup"><span data-stu-id="08058-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="08058-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08058-104">SYNTAX</span></span>

### <span data-ttu-id="08058-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08058-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08058-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08058-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08058-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="08058-107">DESCRIPTION</span></span>
<span data-ttu-id="08058-108">A Reset-AzAttestationPolicy parancsmag alaphelyzetbe állítja a felhasználó által definiált előfizetési házirendet egy bérlői fiókból az Azure Attestation szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="08058-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="08058-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08058-109">EXAMPLES</span></span>

### <span data-ttu-id="08058-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="08058-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="08058-111">Állítsa vissza a házirendet az alapértelmezettre az Attestation Provider *pshtest* for Tee type *SgxEnclave* esetén.</span><span class="sxs-lookup"><span data-stu-id="08058-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="08058-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="08058-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="08058-113">Ha az Attestation Provider *pshtest* az elkülönített megbízhatósági modell használatára van konfigurálva, állítsa vissza a házirendet az alapértelmezettre a Tee típusú *SgxEnclave* esetén egy aláírt házirendet megjelölve.</span><span class="sxs-lookup"><span data-stu-id="08058-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="08058-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08058-114">PARAMETERS</span></span>

### <span data-ttu-id="08058-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08058-115">-DefaultProfile</span></span>
<span data-ttu-id="08058-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08058-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08058-117">-Name</span><span class="sxs-lookup"><span data-stu-id="08058-117">-Name</span></span>
<span data-ttu-id="08058-118">Megadja a bérlő nevét.</span><span class="sxs-lookup"><span data-stu-id="08058-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="08058-119">Ez a parancsmag alaphelyzetbe állítja a paraméter által megadott bérlői házirendet.</span><span class="sxs-lookup"><span data-stu-id="08058-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="08058-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08058-120">-PassThru</span></span>
<span data-ttu-id="08058-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="08058-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="08058-122">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="08058-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="08058-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="08058-123">-Policy</span></span>
<span data-ttu-id="08058-124">A visszaállítható házirenddokumentumot leíró JSON webtoken.</span><span class="sxs-lookup"><span data-stu-id="08058-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="08058-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08058-125">-ResourceGroupName</span></span>
<span data-ttu-id="08058-126">Egy szolgáltató erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="08058-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="08058-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08058-127">-ResourceId</span></span>
<span data-ttu-id="08058-128">Egy szolgáltató Erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="08058-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="08058-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="08058-129">-Tee</span></span>
<span data-ttu-id="08058-130">A megbízható végrehajtási környezet típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="08058-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="08058-131">Négyféle környezettípust támogatunk: SgxEnclave, OpenEnclave, CyResComponent és VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="08058-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="08058-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08058-132">-Confirm</span></span>
<span data-ttu-id="08058-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="08058-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08058-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08058-134">-WhatIf</span></span>
<span data-ttu-id="08058-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="08058-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08058-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="08058-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08058-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08058-137">CommonParameters</span></span>
<span data-ttu-id="08058-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08058-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08058-139">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08058-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08058-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08058-140">INPUTS</span></span>

### <span data-ttu-id="08058-141">System.String</span><span class="sxs-lookup"><span data-stu-id="08058-141">System.String</span></span>

## <span data-ttu-id="08058-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08058-142">OUTPUTS</span></span>

### <span data-ttu-id="08058-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="08058-143">System.Boolean</span></span>

## <span data-ttu-id="08058-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08058-144">NOTES</span></span>

## <span data-ttu-id="08058-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08058-145">RELATED LINKS</span></span>
