---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: f4bf651fd6e5b84714ddb4511365bc0c17c49470
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299837"
---
# <span data-ttu-id="e3538-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="e3538-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="e3538-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3538-102">SYNOPSIS</span></span>
<span data-ttu-id="e3538-103">Visszaállítja a házirendet egy bérlői webhelyről az Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="e3538-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="e3538-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3538-104">SYNTAX</span></span>

### <span data-ttu-id="e3538-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3538-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3538-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3538-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3538-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3538-107">DESCRIPTION</span></span>
<span data-ttu-id="e3538-108">Az Reset-AzAttestationPolicy parancsmag visszaállítja a felhasználó által definiált tanúsítvány-házirendet az Azure tanúsítványban szereplő bérlői webhelyre.</span><span class="sxs-lookup"><span data-stu-id="e3538-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="e3538-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e3538-109">EXAMPLES</span></span>

### <span data-ttu-id="e3538-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e3538-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="e3538-111">Állítsa alaphelyzetbe a házirendet az alapértelmezett értékre a Tee Type *SgxEnclave* hitelesítő szolgáltató *pshtest* .</span><span class="sxs-lookup"><span data-stu-id="e3538-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="e3538-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="e3538-112">Example 2</span></span>
```powershell
PS C:\> $resetJwt = Get-Content -Path .\reset.policy.txt.signed.txt
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $resetJwt
```

<span data-ttu-id="e3538-113">Ha a tanúsítvány-szolgáltató *pshtest* úgy van konfigurálva, hogy az izolált bizalmi modellt használja, a házirendet a Tee Type *SgxEnclave* alapértelmezett értékre kell állítania, ha az aláírt házirendet tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="e3538-113">If the Attestation Provider *pshtest* is configured to use the isolated trust model, reset the policy to the default for Tee type *SgxEnclave* by including a signed policy.</span></span>

## <span data-ttu-id="e3538-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3538-114">PARAMETERS</span></span>

### <span data-ttu-id="e3538-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3538-115">-DefaultProfile</span></span>
<span data-ttu-id="e3538-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3538-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3538-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3538-117">-Name</span></span>
<span data-ttu-id="e3538-118">A bérlő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3538-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="e3538-119">Ez a parancsmag visszaállítja a bérlő által a paraméter által megadott tanúsítvány-házirendet.</span><span class="sxs-lookup"><span data-stu-id="e3538-119">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3538-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3538-120">-PassThru</span></span>
<span data-ttu-id="e3538-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="e3538-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e3538-122">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="e3538-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e3538-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="e3538-123">-Policy</span></span>
<span data-ttu-id="e3538-124">Azt a JSON-webtokent adja meg, amely leírja az alaphelyzetbe állított házirend-dokumentumot.</span><span class="sxs-lookup"><span data-stu-id="e3538-124">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="e3538-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3538-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3538-126">A tanúsítvány-szolgáltató erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3538-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="e3538-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3538-127">-ResourceId</span></span>
<span data-ttu-id="e3538-128">A hitelesítő szolgáltató ResourceID adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3538-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="e3538-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="e3538-129">-Tee</span></span>
<span data-ttu-id="e3538-130">A megbízható végrehajtási környezet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e3538-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="e3538-131">Négy típusú környezetet támogatunk: SgxEnclave, OpenEnclave, CyResComponent és VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="e3538-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="e3538-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3538-132">-Confirm</span></span>
<span data-ttu-id="e3538-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3538-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3538-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3538-134">-WhatIf</span></span>
<span data-ttu-id="e3538-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3538-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3538-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3538-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3538-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3538-137">CommonParameters</span></span>
<span data-ttu-id="e3538-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3538-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3538-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="e3538-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3538-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3538-140">INPUTS</span></span>

### <span data-ttu-id="e3538-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e3538-141">System.String</span></span>

## <span data-ttu-id="e3538-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3538-142">OUTPUTS</span></span>

### <span data-ttu-id="e3538-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3538-143">System.Boolean</span></span>

## <span data-ttu-id="e3538-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3538-144">NOTES</span></span>

## <span data-ttu-id="e3538-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3538-145">RELATED LINKS</span></span>
