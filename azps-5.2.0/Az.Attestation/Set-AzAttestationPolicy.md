---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/set-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Set-AzAttestationPolicy.md
ms.openlocfilehash: c5659dc2234e6305f07de0a2990c76cbc9cd183a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353274"
---
# <span data-ttu-id="3dcc1-101">Set-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="3dcc1-101">Set-AzAttestationPolicy</span></span>

## <span data-ttu-id="3dcc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="3dcc1-103">Beállítja a házirendet egy bérlőtől az Azure Attestationn szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-103">Sets the policy from a tenant in Azure Attestationn.</span></span>

## <span data-ttu-id="3dcc1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3dcc1-104">SYNTAX</span></span>

### <span data-ttu-id="3dcc1-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dcc1-105">NameParameterSet</span></span>
```
Set-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> -Policy <String>
 [-PolicyFormat <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dcc1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dcc1-106">ResourceIdParameterSet</span></span>
```
Set-AzAttestationPolicy [-ResourceId] <String> -Tee <String> -Policy <String> [-PolicyFormat <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dcc1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3dcc1-107">DESCRIPTION</span></span>
<span data-ttu-id="3dcc1-108">A Set-AzAttestationPolicy parancsmag beállítja a házirendet egy bérlőtől az Azure Attestation szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-108">The Set-AzAttestationPolicy cmdlet sets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="3dcc1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3dcc1-109">EXAMPLES</span></span>

### <span data-ttu-id="3dcc1-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="3dcc1-110">Example 1</span></span>
```powershell
PS C:\> $policy = Get-Content -Path .\custom.sgx.policy.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policy
```

<span data-ttu-id="3dcc1-111">Szöveges házirendformátumban (alapértelmezett) beállítja a felhasználó által definiált házirendet az *SgxEnclave* for Attestation Provider *pshtest* szolgáltatóhoz.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-111">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a text policy format (default).</span></span>

### <span data-ttu-id="3dcc1-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="3dcc1-112">Example 2</span></span>
```powershell
PS C:\> $policyjwt = Get-Content -Path .\custom.sgx.policy.jwt.format.txt
PS C:\> Set-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave -Policy $policyjwt -PolicyFormat JWT
```

<span data-ttu-id="3dcc1-113">Az *SgxEnclave* for Attestation Provider *pshtest* felhasználó által definiált házirendet állítja be JWT-házirendformátumban.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-113">Sets the user defined policy for TEE type *SgxEnclave* for Attestation Provider *pshtest* using a JWT policy format.</span></span>

## <span data-ttu-id="3dcc1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3dcc1-114">PARAMETERS</span></span>

### <span data-ttu-id="3dcc1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dcc1-115">-DefaultProfile</span></span>
<span data-ttu-id="3dcc1-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dcc1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3dcc1-117">-Name</span></span>
<span data-ttu-id="3dcc1-118">Megadja a bérlő nevét.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-118">Specifies a name of the tenant.</span></span>
<span data-ttu-id="3dcc1-119">Ez a parancsmag beállítja a paraméterként megadott bérlői webhelyre vonatkozó igazolási házirendet.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-119">This cmdlet sets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="3dcc1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dcc1-120">-PassThru</span></span>
<span data-ttu-id="3dcc1-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3dcc1-122">Ha ez a kapcsoló meg van adva, akkor igaz értéket ad vissza, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3dcc1-123">-Házirend</span><span class="sxs-lookup"><span data-stu-id="3dcc1-123">-Policy</span></span>
<span data-ttu-id="3dcc1-124">A beállított házirenddokumentumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-124">Specifies the policy document to set.</span></span>  <span data-ttu-id="3dcc1-125">A házirend formátuma szöveg vagy JSON webtoken (JWT) lehet.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-125">The policy format can be either Text or JSON Web Token (JWT).</span></span>

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

### <span data-ttu-id="3dcc1-126">-PolicyFormat</span><span class="sxs-lookup"><span data-stu-id="3dcc1-126">-PolicyFormat</span></span>
<span data-ttu-id="3dcc1-127">A házirend formátumát (Szöveg vagy JWT (JSON Web Token) adja meg.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-127">Specifies the format for the policy, either Text or JWT (JSON Web Token).</span></span>  <span data-ttu-id="3dcc1-128">Az alapértelmezett házirendformátum a Szöveg.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-128">The default policy format is Text.</span></span>

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

### <span data-ttu-id="3dcc1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dcc1-129">-ResourceGroupName</span></span>
<span data-ttu-id="3dcc1-130">Egy szolgáltató erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-130">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="3dcc1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dcc1-131">-ResourceId</span></span>
<span data-ttu-id="3dcc1-132">Egy szolgáltató Erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-132">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="3dcc1-133">-Tee</span><span class="sxs-lookup"><span data-stu-id="3dcc1-133">-Tee</span></span>
<span data-ttu-id="3dcc1-134">A megbízható végrehajtási környezet típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-134">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="3dcc1-135">Négyféle környezet támogatott: SgxEnclave, OpenEnclave, CyResComponent és VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-135">Four types of environment are supported: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="3dcc1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dcc1-136">-Confirm</span></span>
<span data-ttu-id="3dcc1-137">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dcc1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dcc1-138">-WhatIf</span></span>
<span data-ttu-id="3dcc1-139">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dcc1-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dcc1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dcc1-141">CommonParameters</span></span>
<span data-ttu-id="3dcc1-142">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dcc1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dcc1-143">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3dcc1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dcc1-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3dcc1-144">INPUTS</span></span>

### <span data-ttu-id="3dcc1-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3dcc1-145">System.String</span></span>

## <span data-ttu-id="3dcc1-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dcc1-146">OUTPUTS</span></span>

### <span data-ttu-id="3dcc1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3dcc1-147">System.String</span></span>

## <span data-ttu-id="3dcc1-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3dcc1-148">NOTES</span></span>

## <span data-ttu-id="3dcc1-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dcc1-149">RELATED LINKS</span></span>
