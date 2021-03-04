---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestationpolicysigner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestationPolicySigner.md
ms.openlocfilehash: e0b86a1cd7c3e1355cfc760fecc257b3cde87561
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926018"
---
# <span data-ttu-id="ec0d1-101">Remove-AzAttestationPolicySigner</span><span class="sxs-lookup"><span data-stu-id="ec0d1-101">Remove-AzAttestationPolicySigner</span></span>

## <span data-ttu-id="ec0d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec0d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0d1-103">Eltávolítja egy bérlő megbízható házirend-aláíróját az Azure Attestation szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-103">Removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="ec0d1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec0d1-104">SYNTAX</span></span>

### <span data-ttu-id="ec0d1-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec0d1-105">NameParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-Name] <String> [-ResourceGroupName] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec0d1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec0d1-106">ResourceIdParameterSet</span></span>
```
Remove-AzAttestationPolicySigner [-ResourceId] <String> -Signer <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec0d1-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec0d1-107">DESCRIPTION</span></span>
<span data-ttu-id="ec0d1-108">A Remove-AzAttestationPolicySigner parancsmag eltávolítja egy bérlő megbízható házirend-aláíróját az Azure Attestation szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-108">The Remove-AzAttestationPolicySigner cmdlet removes a trusted policy signer for a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="ec0d1-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec0d1-109">EXAMPLES</span></span>

### <span data-ttu-id="ec0d1-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ec0d1-110">Example 1</span></span>
```powershell
PS C:\> $trustedSigner = Get-Content -Path .\trusted.signer.txt
PS C:\> Remove-AzAttestationPolicySigner -Name pshtest -ResourceGroupName psh-test-rg -Signer $trustedSigner
```

<span data-ttu-id="ec0d1-111">Távolítsa el a pshtest nevű szolgáltató megbízható *aláíróját.*</span><span class="sxs-lookup"><span data-stu-id="ec0d1-111">Remove a trusted signer for the Attestation Provider named *pshtest*.</span></span>

## <span data-ttu-id="ec0d1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec0d1-112">PARAMETERS</span></span>

### <span data-ttu-id="ec0d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0d1-113">-DefaultProfile</span></span>
<span data-ttu-id="ec0d1-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec0d1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ec0d1-115">-Name</span></span>
<span data-ttu-id="ec0d1-116">Egy szolgáltató nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-116">Specifies the name of an attestation provider.</span></span>

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

### <span data-ttu-id="ec0d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec0d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="ec0d1-118">Egy szolgáltató erőforráscsoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-118">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="ec0d1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0d1-119">-ResourceId</span></span>
<span data-ttu-id="ec0d1-120">Egy szolgáltató Erőforrásazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-120">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="ec0d1-121">-Aláíró</span><span class="sxs-lookup"><span data-stu-id="ec0d1-121">-Signer</span></span>
<span data-ttu-id="ec0d1-122">Azt az RFC7519 JSON web tokent adja meg, amely egy "maa-policyCertificate" nevű igénylést tartalmaz, amelynek értéke egy RFC7517 JSON webkulcs, amely egy eltávolítható megbízható aláíró kulcsot tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-122">Specifies the RFC7519 JSON Web Token containing a claim named "maa-policyCertificate" whose value is an RFC7517 JSON Web Key which contains a trusted signing key to remove.</span></span>
<span data-ttu-id="ec0d1-123">Az RFC7519 JWT-t a meglévő megbízható aláíró kulcsok egyikében kell aláírni.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-123">The RFC7519 JWT must be signed with one of the existing trusted signing keys.</span></span>

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

### <span data-ttu-id="ec0d1-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec0d1-124">-Confirm</span></span>
<span data-ttu-id="ec0d1-125">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec0d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec0d1-126">-WhatIf</span></span>
<span data-ttu-id="ec0d1-127">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec0d1-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec0d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0d1-129">CommonParameters</span></span>
<span data-ttu-id="ec0d1-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec0d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0d1-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec0d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0d1-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec0d1-132">INPUTS</span></span>

### <span data-ttu-id="ec0d1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ec0d1-133">System.String</span></span>

## <span data-ttu-id="ec0d1-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec0d1-134">OUTPUTS</span></span>

### <span data-ttu-id="ec0d1-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span><span class="sxs-lookup"><span data-stu-id="ec0d1-135">Microsoft.Azure.Commands.Attestation.Models.PSPolicySigners</span></span>

## <span data-ttu-id="ec0d1-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec0d1-136">NOTES</span></span>

## <span data-ttu-id="ec0d1-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec0d1-137">RELATED LINKS</span></span>
