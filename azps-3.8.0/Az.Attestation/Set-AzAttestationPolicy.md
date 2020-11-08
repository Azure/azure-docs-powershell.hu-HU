---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012725"
---
# <span data-ttu-id="be783-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="be783-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="be783-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be783-102">SYNOPSIS</span></span>
<span data-ttu-id="be783-103">A házirendet az Azure Attestationn-beli bérlői fiókban állítja be.</span><span class="sxs-lookup"><span data-stu-id="be783-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="be783-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be783-104">SYNTAX</span></span>

### <span data-ttu-id="be783-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="be783-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be783-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be783-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be783-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="be783-107">DESCRIPTION</span></span>
<span data-ttu-id="be783-108">Az Set-AzAttestationPolicy parancsmag az Azure-tanúsítványban lévő bérlői fiókra állítja be a házirendet.</span><span class="sxs-lookup"><span data-stu-id="be783-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="be783-109">Példák</span><span class="sxs-lookup"><span data-stu-id="be783-109">EXAMPLES</span></span>

### <span data-ttu-id="be783-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="be783-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="be783-111">A felhasználó által definiált házirend beállítása a TEE Type *SgxEnclave* a tanúsítvány-szolgáltató *pshtest* szöveges házirend-formátummal (alapértelmezett).</span><span class="sxs-lookup"><span data-stu-id="be783-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="be783-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="be783-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="be783-113">Beállítja a felhasználó által definiált házirendet a TEE Type *SgxEnclave* a hitelesítő szolgáltató *pshtest* a JWT házirend-formátum használatával.</span><span class="sxs-lookup"><span data-stu-id="be783-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="be783-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be783-114">PARAMETERS</span></span>

### <span data-ttu-id="be783-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be783-115">-DefaultProfile</span></span>
<span data-ttu-id="be783-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be783-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be783-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="be783-117">-Name</span></span>
<span data-ttu-id="be783-118">A bérlő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be783-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="be783-119">Ez a parancsmag a fenti paraméter által megadott bérlői tanúsítvány-házirendet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="be783-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="be783-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be783-120">-PassThru</span></span>
<span data-ttu-id="be783-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="be783-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="be783-122">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="be783-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="be783-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="be783-123">-Policy</span></span>
<span data-ttu-id="be783-124">Megadja a beállítani kívánt házirend-dokumentumot.</span><span class="sxs-lookup"><span data-stu-id="be783-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="be783-125">A házirend-formátum lehet szöveges vagy JSON webes jogkivonat (JWT).</span><span class="sxs-lookup"><span data-stu-id="be783-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="be783-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="be783-126">-PolicyFormat</span></span>
<span data-ttu-id="be783-127">A házirend formátumát adja meg szöveg vagy JWT (JSON web token) esetén.</span><span class="sxs-lookup"><span data-stu-id="be783-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="be783-128">Az alapértelmezett házirend-formátum a szöveg.</span><span class="sxs-lookup"><span data-stu-id="be783-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="be783-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be783-129">-ResourceGroupName</span></span>
<span data-ttu-id="be783-130">A tanúsítvány-szolgáltató erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be783-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="be783-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be783-131">-ResourceId</span></span>
<span data-ttu-id="be783-132">A hitelesítő szolgáltató ResourceID adja meg.</span><span class="sxs-lookup"><span data-stu-id="be783-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="be783-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="be783-133">-Tee</span></span>
<span data-ttu-id="be783-134">A megbízható végrehajtási környezet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="be783-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="be783-135">A következő négy típusú környezet támogatott: SgxEnclave, OpenEnclave, CyResComponent és VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="be783-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="be783-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="be783-136">-Confirm</span></span>
<span data-ttu-id="be783-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="be783-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be783-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be783-138">-WhatIf</span></span>
<span data-ttu-id="be783-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="be783-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be783-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="be783-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be783-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be783-141">CommonParameters</span></span>
<span data-ttu-id="be783-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be783-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be783-143">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="be783-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be783-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be783-144">INPUTS</span></span>

### <span data-ttu-id="be783-145">System. String</span><span class="sxs-lookup"><span data-stu-id="be783-145">System.String</span></span>

## <span data-ttu-id="be783-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be783-146">OUTPUTS</span></span>

### <span data-ttu-id="be783-147">System. String</span><span class="sxs-lookup"><span data-stu-id="be783-147">System.String</span></span>

## <span data-ttu-id="be783-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be783-148">NOTES</span></span>

## <span data-ttu-id="be783-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be783-149">RELATED LINKS</span></span>
